---
layout: page
title: contact
permalink: /contact/
nav: true
nav_order: 6
---

<div class="contact-page">
  <h2>Let's Connect</h2>
  
  <p>Hello! Thanks for wanting to get in touch - I appreciate your interest! Here's how you can reach me most effectively.</p>
  
  <p><strong>Please read through these details before contacting me!</strong> - it'll help us both! Email is my preferred way to connect.</p> 
  
  <p>You can follow me on social media for updates.</p>
  
  <ul>
    <li><strong>LinkedIn:</strong>  <style>
        .libutton {
          display: flex;
          flex-direction: column;
          justify-content: center;
          padding: 7px;
          text-align: center;
          outline: none;
          text-decoration: none !important;
          color: #ffffff !important;
          width: 200px;
          height: 32px;
          border-radius: 16px;
          background-color: #0A66C2;
          font-family: "SF Pro Text", Helvetica, sans-serif;
        }
      </style>
        <a class="libutton" href="https://www.linkedin.com/comm/mynetwork/discovery-see-all?usecase=PEOPLE_FOLLOWS&followMember=tolgahan" target="_blank">Follow on LinkedIn</a></li>
    <li><strong>X:</strong> <a href="https://twitter.com/t_cakaloglu" target="_blank">@t_cakaloglu</a></li>
    <li><strong>Bluesky:</strong> <a href="https://bsky.app/profile/tolgahanai.bsky.social" target="_blank">@tolgahanai.bsky.social</a></li>
  </ul>

  <h3>How to get in touch?</h3>
  
  <p>In most cases, email is the best way to reach me: <strong>firstname at lastname dot org</strong>.</p>
  
  <p> I used to reply to every non-spam email I received, but with my current workload, that's no longer possible. I've noticed I spend a lot of time:</p>
  <ul>
    <li>answering emails with standard responses</li>
    <li>asking for missing details that weren't included initially</li>
  </ul>
  <p>To help us both communicate more efficiently, I've outlined common inquiry types below and the best way to handle each:</p>
  <ul>
    <li><a href='#talk-invitations'><u>Talk Invitations</u></a></li>
    <li><a href='#collaboration-requests'><u>Collaboration requests</u></a></li>
  </ul>
  <h3 id="talk-invitations">Talk invitations</h3>
  
  <p>Thank you so much for your interest! The value of research and experience certainly diminishes without properly communicating it and empowering others to use it. Hence, I welcome any relevant talk opportunities. <strong>Please note that I cannot discuss proprietary projects, data, or any confidential information related to my current organization. However, I'm happy to offer a field-wide perspective, drawing on publicly available research and my expertise in AI & ML.</strong></p>
  
  <p>I typically accept in-person speaking invitations since I've found them much more effective than virtual presentations. I'm open to traveling for talks when the necessary arrangements can be accommodated.</p>
  
  <p>To help me evaluate your speaking invitation, please include these details in your message:</p>
  <ul>
    <li><strong>Event format and setting:</strong> Will this be an academic presentation, conference keynote, workshop session, or media interview? Please specify if it's planned as an in-person event and the location.</li>
    <li><strong>Target audience profile:</strong> Who will be attending? If you have suggestions for relevant presentation themes that would suit this group, I'd appreciate hearing them.</li>
    <li><strong>Preferred timing and flexibility:</strong> What dates work best for your event? How adaptable can you be with scheduling if needed?</li>
  </ul>
  <p>You might find it useful to review my previous presentations on my updates page to understand the range of topics I typically cover.</p>

  <h3 id="collaboration-requests">Collaboration requests</h3>
  
  <p>I appreciate your interest in potential collaboration! </p>
  
  <p><strong> * Unfortunately, I won't be taking on any collaboration requests during this time.</strong></p>

  <p>Typically, while I enjoy exploring new research opportunities, I can only commit to a limited number of partnerships annually. These must align closely with my current research focus. Please note that I cannot provide organizational hosting or computational resources for collaborative projects.</p>
  <p>To help me evaluate your proposal, please include:</p>
  <ul>
    <li><strong>Research focus and objectives:</strong> Even without a detailed plan, clearly indicate which research domain interests you and what you hope to investigate.</li>
    <li><strong>Your motivation and background:</strong> Explain your interest in this area and highlight relevant experience or prior work. New researchers are welcome, but please demonstrate genuine commitment to the field.</li>
    <li><strong>Connection to my work:</strong> Reference specific publications or presentations of mine that relate to your proposed research direction.</li>
  </ul>
  <p>In most recent partnerships, my involvement typically includes strategic guidance through regular discussions, project direction, promotional support, and collaborative writing.</p>

  <!-- <h3>Internship applications</h3>
  
  <p>I appreciate your interest in pursuing a career opportunity with me.</p>
  <p><strong> * Unfortunately, I won't be taking on any intern positions during this time.</strong></p> -->

  <h3>Contact Form</h3>
  
  <p>Or if you want to reach out feel free to message me here:</p>
  
  <!-- Using Formspree form endpoint -->
  <form class="contact-form" action="https://formspree.io/f/mrblqgdz" method="POST">
    <div class="form-group">
      <label for="first-name">First name*</label>
      <input type="text" id="first-name" name="first-name" required>
    </div>
    
    <div class="form-group">
      <label for="last-name">Last name*</label>
      <input type="text" id="last-name" name="last-name" required>
    </div>
    
    <div class="form-group">
      <label for="email">Email*</label>
      <input type="email" id="email" name="_replyto" required>
    </div>
    
    <div class="form-group">
      <label for="message">Message</label>
      <textarea id="message" name="message" rows="6" required></textarea>
    </div>
    
    <!-- Hidden field for Formspree -->
    <input type="hidden" name="_next" value="{{ site.url }}{{ site.baseurl }}/contact/?success=true">
    
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
  
  <!-- Success message (will show when form is submitted successfully) -->
  <div id="success-message" style="display: none; margin-top: 1rem; padding: 1rem; background-color: #d4edda; border: 1px solid #c3e6cb; border-radius: 4px; color: #155724;">
    <p><strong>Thank you!</strong> Your message has been sent successfully. I'll get back to you soon.</p>
  </div>
  
  <script>
    // Show success message if URL contains success parameter
    if (window.location.search.includes('success=true')) {
      document.getElementById('success-message').style.display = 'block';
    }
  </script>
</div>
