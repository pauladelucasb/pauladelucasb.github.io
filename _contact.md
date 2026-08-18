---
title: "Contact"
permalink: /contact/
author_profile: true
---
## Direct

pd758@georgetown.edu

Department of Spanish and Portuguese

Georgetown University
Washington, DC

## Contact Form

<form id="contactForm">
  <div style="margin-bottom: 15px;">
    <label for="name">Name:</label><br>
    <input type="text" id="name" name="name" required style="width: 100%; padding: 8px; border: 1px solid #ccc; border-radius: 4px;">
  </div>

  <div style="margin-bottom: 15px;">
    <label for="email">Email:</label><br>
    <input type="email" id="email" name="email" required style="width: 100%; padding: 8px; border: 1px solid #ccc; border-radius: 4px;">
  </div>

  <div style="margin-bottom: 15px;">
    <label for="message">Message:</label><br>
    <textarea id="message" name="message" rows="6" required style="width: 100%; padding: 8px; border: 1px solid #ccc; border-radius: 4px;"></textarea>
  </div>

  <button type="submit" style="background-color: #0092ca; color: white; padding: 10px 20px; border: none; border-radius: 4px; cursor: pointer; font-size: 16px;">Send Message</button>
</form>

<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/index.min.js"></script>
<script type="text/javascript">
  emailjs.init('YOUR_PUBLIC_KEY');
  
  document.getElementById('contactForm').addEventListener('submit', function(event) {
    event.preventDefault();
    
    emailjs.send('service_id', 'template_id', {
      to_email: 'pd758@georgetown.edu',
      from_name: document.getElementById('name').value,
      from_email: document.getElementById('email').value,
      message: document.getElementById('message').value
    }).then(function(response) {
      alert('Message sent successfully!');
      document.getElementById('contactForm').reset();
    }, function(error) {
      alert('Failed to send message. Please try again.');
    });
  });
</script>
