---
layout: service
title: Sales Clarity & Performance Retreat – Jekyll Island
tagline: Step away to move forward.
price: "$10,000 total engagement (30-day onsite partnership)"
image: /assets/img/services/sales-retreat.webp
---

## Description
The **Sales Clarity & Performance Retreat** helps sales teams rediscover clarity, confidence, and communication. This immersive 30-day engagement begins with a 4-day offsite retreat on Jekyll Island, Georgia — a place where teams step away from routine to rebuild focus, trust, and performance.  

We blend audit-level insight, human-centered coaching, and operational alignment to help teams sell with both purpose and peace.

## Tags
Sales Coaching · Team Development · Leadership Clarity · Organizational Renewal

---

## What’s Included
- 4-day offsite retreat with customized team workshops  
- Pre-retreat discovery and system review  
- Post-retreat accountability and performance integration  
- CRM and KPI alignment recommendations  
- Individual and group coaching sessions  

## Why It Works
- Balances clarity, accountability, and humanity  
- Eliminates root causes of underperformance  
- Replaces over-accountability with trust and alignment  
- Teaches teams to thrive sustainably — even in challenging markets  

## Who This Is For
- Sales teams in need of culture and communication resets  
- Organizations experiencing burnout or turnover due to over-accountability  
- Leaders seeking operational clarity and stronger team connection  
- Businesses that value sustainable, human-centered growth  

## Retreat Schedule
- **Day 1 – Arrival & Grounding:** Welcome dinner, sunset reflection walk, purpose setting  
- **Day 2 – Listening & Alignment:** Workshops on empathy, communication, and culture reset  
- **Day 3 – Systems & Strengths:** CRM audit, process design, and team discussion around balance  
- **Day 4 – Commitment & Closure:** Action planning, next-step commitments, farewell brunch  

## Pricing
- $10,000 total engagement (30-day Sales Clarity & Performance System)  
- $1,500 per participant retreat package (lodging, meals, and materials included)  
- Optional add-ons: leadership dinner, video recap, or private coaching sessions  
- Travel coordination included (15–20% built-in margin)  

> *“Peace is the pathway to performance. When sales teams rediscover calm, they rediscover clarity.”*

<button id="startProcessBtn" class="btn">Start Your Retreat Inquiry</button>

<!-- Modal Overlay -->
<div id="formModal" class="form-modal">
  <div class="form-content">
    <button class="close-modal" aria-label="Close Form">&times;</button>
    <form action="https://formspree.io/f/mldpwzwy" method="POST" class="sales-retreat-form">
      <input type="hidden" name="service" value="Sales Clarity & Performance Retreat">
      <h3>Retreat Inquiry Form</h3>
      <p>Thank you for your interest in the Sales Clarity & Performance Retreat. This form helps us understand your team, goals, and what you hope to accomplish during the 30-day engagement. All inquiries are <strong>confidential</strong>.</p>

      <!-- Organization Info -->
      <h4>Organization Information</h4>
      <label>Organization Name:<br><input type="text" name="organization" required></label><br>
      <label>Contact Name:<br><input type="text" name="contact_name" required></label><br>
      <label>Email:<br><input type="email" name="email" required></label><br>
      <label>Phone:<br><input type="tel" name="phone"></label><br>

      <!-- Retreat Details -->
      <h4>Retreat Details</h4>
      <label>Team Size:<br><input type="number" name="team_size" min="1"></label><br>
      <label>Preferred Start Date:<br><input type="date" name="start_date"></label><br>
      <label>Key Goals or Challenges:<br><textarea name="goals" rows="3"></textarea></label><br>
      <label>Additional Notes:<br><textarea name="notes" rows="3"></textarea></label><br>

      <!-- Confidentiality -->
      <p class="disclaimer"><strong>Confidentiality Notice:</strong> All submissions are private and reviewed only by Street Light Consulting. We never share your information without consent.</p>

      <!-- Honeypot -->
      <label class="visually-hidden">Leave this field empty<input type="text" name="_gotcha" tabindex="-1" autocomplete="off"></label>

      <button type="submit">Submit Inquiry</button>
    </form>
  </div>
</div>

<!-- Success Message Overlay -->
<div id="successOverlay" class="success-overlay">
  <div class="success-content">
    <h3>✅ Inquiry Received</h3>
    <p>Thank you for reaching out about the Sales Clarity & Performance Retreat. We’ll review your information and respond soon to discuss next steps.</p>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const startBtn = document.getElementById("startProcessBtn");
  const modal = document.getElementById("formModal");
  const closeBtn = modal.querySelector(".close-modal");
  const successOverlay = document.getElementById("successOverlay");
  const form = modal.querySelector("form");

  startBtn.addEventListener("click", () => modal.classList.add("show"));
  closeBtn.addEventListener("click", () => modal.classList.remove("show"));
  modal.addEventListener("click", (e) => { if (e.target === modal) modal.classList.remove("show"); });

  form.addEventListener("submit", async (e) => {
    e.preventDefault();
    const formData = new FormData(form);
    try {
      const response = await fetch(form.action, {
        method: form.method,
        body: formData,
        headers: { 'Accept': 'application/json' }
      });
      if (response.ok) {
        modal.classList.remove("show");
        successOverlay.classList.add("show");
        form.reset();
        setTimeout(() => successOverlay.classList.remove("show"), 4000);
      } else {
        alert("There was an issue submitting your inquiry. Please try again.");
      }
    } catch {
      alert("Network error. Please try again later.");
    }
  });
});
</script>
