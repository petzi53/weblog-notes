---
description: contact form
title: Contact me
disable_comments: true
no_coins: true
---

<form action="https://formspree.io/peter.baumgartner@icloud.com" method="POST">
  <input type="text" name="name" required="required" placeholder="Your name"><br>
  <input type="email" name="_replyto" required="required" placeholder="Your email address"><br>
  <textarea rows="4" name="message" id="message" required="required" class="form-control" placeholder="Write here your message to me!"></textarea>
  <input type="hidden" name="_next" value="/thanks" />
  <input type="submit" value="Send" name="submit" class="btn btn-primary btn-outline">
  <input type="hidden" name="_subject" value="[Notes-Blog]: Contact page" />
  <input type="text" name="_gotcha" style="display:none" />
</form>
