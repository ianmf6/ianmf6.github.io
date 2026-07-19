---
title: Contact
permalink: /contact/
layout: single
#author_profile: false
---

Questions, feedback, a bug in one of my apps, or anything about a project or post — use the form below.

It posts straight to my self-hosted server: no Google, no trackers, nothing stored in your browser.

<style>
.cf-row{margin:0 0 16px}
.cf-row label{display:block;font-weight:600;font-size:.85em;margin-bottom:4px}
.cf-row label span{font-weight:400;color:#767676}
.cf-row input,.cf-row select,.cf-row textarea{width:100%;box-sizing:border-box;padding:9px 11px;font:inherit;font-size:.9em;border:1px solid #b6b6b6;border-radius:6px;background:#fff;color:#222}
.cf-row textarea{resize:vertical;min-height:160px}
.cf-row input:focus,.cf-row select:focus,.cf-row textarea:focus{outline:2px solid #0a7ea4;outline-offset:1px;border-color:#0a7ea4}
.cf-count{font-size:.75em;color:#767676;text-align:right;margin-top:3px}
.cf-hp{position:absolute !important;left:-9999px !important;top:-9999px !important;opacity:0;height:0;overflow:hidden}
#cf-send{display:inline-block;font:inherit;font-size:.9em;font-weight:600;color:#fff;background:#0a7ea4;border:0;border-radius:6px;padding:10px 22px;cursor:pointer}
#cf-send:hover{background:#086b8c}
#cf-send[disabled]{opacity:.6;cursor:default}
#cf-status{font-size:.9em;margin-top:12px}
#cf-status.cf-err{color:#c0392b;font-weight:600}
#cf-ok{border:1px solid #b6d7c4;background:#eef7f1;color:#1c6b3c;border-radius:8px;padding:16px 18px;margin:8px 0 16px}
.cf-note{font-size:.75em;color:#767676;margin-top:14px}
</style>

<div id="cf-ok" hidden>
  <strong>Thanks — your message is on its way.</strong><br>
  If you left an email address, I'll reply there.
</div>

<form id="cf" novalidate>
  <div class="cf-row">
    <label for="cf-name">Name <span>(optional)</span></label>
    <input id="cf-name" type="text" maxlength="80" autocomplete="name">
  </div>
  <div class="cf-row">
    <label for="cf-email">Email <span>(optional — only if you'd like a reply)</span></label>
    <input id="cf-email" type="email" maxlength="200" autocomplete="email" placeholder="you@example.com">
  </div>
  <div class="cf-row">
    <label for="cf-topic">Topic</label>
    <select id="cf-topic">
      <option value="other" selected>General / something else</option>
      <option value="support">Question</option>
      <option value="bug">Bug report</option>
      <option value="feature">Feature request</option>
    </select>
  </div>
  <div class="cf-row">
    <label for="cf-msg">Message</label>
    <textarea id="cf-msg" maxlength="3800" required></textarea>
    <div class="cf-count" id="cf-count">0 / 3800</div>
  </div>
  <div class="cf-hp" aria-hidden="true">
    <label for="cf-web">Leave this field empty</label>
    <input id="cf-web" type="text" tabindex="-1" autocomplete="off">
  </div>
  <button type="submit" id="cf-send">Send message</button>
  <p id="cf-status" role="status"></p>
</form>

<p class="cf-note">Sent over HTTPS to my own server — no third parties involved. Your message and optional
email are used only to read and answer it, never for marketing or profiling.</p>

<noscript><p><em>This form needs JavaScript to send. My apps also have a built-in
<strong>Contact Me</strong> screen that reaches me the same way.</em></p></noscript>

<script>
(function () {
  var API = "https://apps.ianm.tech/api/feedback";
  var KEY = "7eb0cb662855c08357af02deecbee576d7a6cefa518863a7cb458f518b123bc8"; // public by design — identifies this form, grants nothing
  var EMAIL_RE = /^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$/;

  var form = document.getElementById("cf");
  var okBox = document.getElementById("cf-ok");
  var status = document.getElementById("cf-status");
  var send = document.getElementById("cf-send");
  var msgEl = document.getElementById("cf-msg");
  var countEl = document.getElementById("cf-count");

  msgEl.addEventListener("input", function () {
    countEl.textContent = msgEl.value.length + " / 3800";
  });

  function uuid() {
    if (window.crypto && crypto.randomUUID) return crypto.randomUUID();
    var b = crypto.getRandomValues(new Uint8Array(16));
    b[6] = (b[6] & 15) | 64; b[8] = (b[8] & 63) | 128;
    var h = "";
    for (var i = 0; i < 16; i++) {
      if (i === 4 || i === 6 || i === 8 || i === 10) h += "-";
      h += b[i].toString(16).padStart(2, "0");
    }
    return h;
  }

  function fail(text) {
    status.className = "cf-err";
    status.textContent = text;
    send.disabled = false;
    send.textContent = "Send message";
  }

  form.addEventListener("submit", function (e) {
    e.preventDefault();

    // Honeypot: humans never see this field. Pretend success so bots move on.
    if (document.getElementById("cf-web").value) {
      form.hidden = true; okBox.hidden = false;
      return;
    }

    var name = document.getElementById("cf-name").value.trim();
    var email = document.getElementById("cf-email").value.trim();
    var message = msgEl.value.trim();

    if (!message) { fail("Please write a message first."); return; }
    if (email && !EMAIL_RE.test(email)) {
      fail("That email address doesn't look right — fix it or leave it empty.");
      return;
    }
    if (name) message = "From: " + name + "\n\n" + message;
    // The server caps the message at 4000 BYTES (not characters).
    if (new TextEncoder().encode(message).length > 4000) {
      fail("Your message is a little too long — please shorten it.");
      return;
    }

    var payload = {
      v: 1,
      install_id: uuid(),          // random per submission — deliberately not stored
      app_version: "1.0.0",        // version of this form's contract, not of any app
      category: document.getElementById("cf-topic").value,
      message: message
    };
    if (email) payload.contact = email;

    send.disabled = true;
    send.textContent = "Sending…";
    status.className = "";
    status.textContent = "";

    fetch(API, {
      method: "POST",
      headers: { "Content-Type": "application/json", "X-API-Key": KEY },
      body: JSON.stringify(payload)
    }).then(function (res) {
      if (res.ok) {
        form.hidden = true;
        okBox.hidden = false;
        okBox.scrollIntoView({ block: "nearest" });
      } else if (res.status === 429) {
        fail("The send limit was reached — please try again in a little while.");
      } else {
        fail("Couldn't send right now — please try again in a few minutes.");
      }
    }).catch(function () {
      fail("Couldn't reach the server — check your connection and try again.");
    });
  });
})();
</script>
