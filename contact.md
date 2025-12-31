---
layout: default
title: Contact Me
---
# Contact Me

<div style="background-color: #f6f8fa; padding: 20px; border-radius: 6px; border: 1px solid #e1e4e8;">
  <h3>Schedule a Strategic Consultation</h3>
  <p>Fill out the details below to start the conversation.</p>
  
  <label for="senderName" style="display:block; margin-bottom: 5px;"><strong>Name</strong></label>
  <input type="text" id="senderName" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px;">

  <label for="senderEmail" style="display:block; margin-bottom: 5px;"><strong>Email</strong></label>
  <input type="text" id="senderEmail" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px;">

  <label for="emailSubject" style="display:block; margin-bottom: 5px;"><strong>Subject</strong></label>
  <input type="text" id="emailSubject" value="Strategic Consultation Inquiry" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px;">
  
  <label for="emailBody" style="display:block; margin-bottom: 5px;"><strong>Message</strong></label>
  <textarea id="emailBody" rows="6" style="width: 100%; padding: 8px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 4px;">Hi Krzysztof,

I'm interested in discussing...</textarea>
  
  <button onclick="sendEmail()" style="background-color: #2ea44f; color: white; padding: 10px 20px; border: none; border-radius: 6px; font-size: 16px; font-weight: bold; cursor: pointer;">Send Email Request</button>
  
  <p style="margin-top: 15px; font-size: 0.9em;">
    Prefer to use your own client? <a href="mailto:kjrogowski@yahoo.com">Email me at kjrogowski@yahoo.com</a>
  </p>
</div>

<script>
function sendEmail() {
    var name = document.getElementById('senderName').value;
    var email = document.getElementById('senderEmail').value;
    var subject = encodeURIComponent(document.getElementById('emailSubject').value);
    var message = document.getElementById('emailBody').value;
    var body = encodeURIComponent("Name: " + name + "\nEmail: " + email + "\n\n" + message);
    window.location.href = "mailto:kjrogowski@yahoo.com?subject=" + subject + "&body=" + body;
}
</script>