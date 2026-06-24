---
layout: page
title: Contact
permalink: /contact/
---

Use the form below to get in touch.


<form class="contact-form" action="https://formsubmit.co/abinrimal7@gmail.com" method="POST">
  <input type="hidden" name="_subject" value="New message from abinrimal.github.io contact form">
  <input type="hidden" name="_captcha" value="false">
  <input type="hidden" name="_template" value="table">
  <input type="text" name="_honey" class="contact-honeypot" tabindex="-1" autocomplete="off">

  <label for="contact-name">Name</label>
  <input id="contact-name" type="text" name="name" required>

  <label for="contact-email">Email</label>
  <input id="contact-email" type="email" name="email" required>

  <label for="contact-subject">Subject</label>
  <input id="contact-subject" type="text" name="subject" required>

  <label for="contact-message">Message</label>
  <textarea id="contact-message" name="message" rows="7" required></textarea>

  <div class="recaptcha-wrap">
    <div class="g-recaptcha" data-sitekey="{{ site.recaptcha_site_key | default: '6LdAgyYtAAAAAOBPb-h2H1luDJj35gD-1MJ-HH_7' }}"></div>
    <p class="recaptcha-error" hidden>Please complete the reCAPTCHA verification before sending.</p>
  </div>

  <button class="button" type="submit">Send Message</button>
</form>

<p class="contact-note">
  Verify that you are human using the checkbox above, then submit the form.
</p>

<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<script>
  document.addEventListener('DOMContentLoaded', function () {
    var contactForm = document.querySelector('.contact-form');
    var errorMessage = document.querySelector('.recaptcha-error');

    if (!contactForm || !errorMessage) {
      return;
    }

    contactForm.addEventListener('submit', function (event) {
      var recaptchaResponse = '';

      if (typeof grecaptcha !== 'undefined') {
        recaptchaResponse = grecaptcha.getResponse();
      }

      if (!recaptchaResponse) {
        event.preventDefault();
        errorMessage.hidden = false;
      } else {
        errorMessage.hidden = true;
      }
    });
  });
</script>
