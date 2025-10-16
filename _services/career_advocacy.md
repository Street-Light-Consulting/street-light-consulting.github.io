---
layout: service
title: Career Representation & Advocacy
tagline: We help people find employers that actually care.
price: "$400/month ($200 due at signing, $200 success fee after 90 days)"
image: /assets/img/services/advocacy.webp
---

## Description
Street Light Recruiting offers **Career Representation & Advocacy** — a candidate-first recruiting model for professionals seeking workplaces that value integrity, purpose, and people. We act as your personal agent, helping you find employers who treat you with respect and fairness while guiding you through each step of your career search.

No algorithms. No mass submissions. Just real advocacy for real people.

## Tags
Career Guidance · Professional Representation · Ethical Recruiting

---

## What’s Included
- Dedicated representation and introductions to vetted employers  
- Resume and profile refinement  
- Employer culture screening  
- Offer review and negotiation guidance  
- 90-day follow-up to ensure satisfaction and stability  

## Why It Works
- You are the client — not the company  
- Every employer is screened for culture, fairness, and respect  
- You approve all submissions before introductions  
- Integrity and trust guide every step  

## Who This Is For
- Mid-level and executive professionals burned out by corporate culture  
- Individuals seeking meaningful, healthy work environments  
- Professionals tired of impersonal job boards and ghosting  
- People ready for a reset — and an advocate who listens  

## Pricing
- $400/month — $200 due at signing, $200 success fee after 90 days  
- Cancel anytime before placement  
- Includes resume/profile review, advocacy, and placement support  
- Optional ongoing coaching available after placement  

> *“The integrity of the upright guides them.” — Proverbs 11:3*

<button id="startProcessBtn" class="btn">Start Your Representation Application</button>

<!-- Modal Overlay -->
<div id="formModal" class="form-modal">
  <div class="form-content">
    <button class="close-modal" aria-label="Close Form">&times;</button>
    <form action="https://formspree.io/f/mldpwzwy" method="POST" class="career-representation-form">
      <input type="hidden" name="service" value="Career Representation & Advocacy">
      <h3>Representation Application</h3>
      <p>Thank you for your interest in working with Street Light. This form helps us understand your professional goals, strengths, and the kind of workplace you want to be part of. All inquiries are <strong>confidential</strong> and never shared with employers without your consent.</p>

      <!-- Candidate Info -->
      <h4>Personal & Contact Information</h4>
      <label>Full Name:<br><input type="text" name="name" required></label><br>
      <label>Email:<br><input type="email" name="email" required></label><br>
      <label>Phone:<br><input type="tel" name="phone"></label><br>
      <label>LinkedIn or Resume URL:<br><input type="url" name="linkedin"></label><br>

      <!-- Career Preferences -->
      <h4>Career Goals & Preferences</h4>
      <label>Desired Role or Industry:<br><input type="text" name="desired_role" required></label><br>
      <label>Preferred Work Location (Remote/Hybrid/Onsite):<br><input type="text" name="location_preference"></label><br>
      <label>Salary Range:<br><input type="text" name="salary_range" placeholder="$XX,XXX – $YY,YYY"></label><br>
      <label>Top Strengths & Skills:<br><textarea name="strengths" rows="3"></textarea></label><br>
      <label>Describe Your Ideal Work Environment:<br><textarea name="environment" rows="3"></textarea></label><br>
      <label>Dealbreakers or Red Flags You Want to Avoid:<br><textarea name="dealbreakers" rows="3"></textarea></label><br>

      <!-- Motivation -->
      <h4>Your Motivation</h4>
      <label>Why are you seeking representation at this time?<br><textarea name="motivation" rows="3"></textarea></label><br>
      <label>How did you hear about Street Light?<br><input type="text" name="referral"></label><br>

      <!-- Confidentiality -->
      <p class="disclaimer"><strong>Confidentiality Notice:</strong> All submissions are private and reviewed only by Street Light Consulting. We never share your information or reach out to employers without your permission.</p>

      <!-- Honeypot -->
      <label class="visually-hidden">Leave this field empty<input type="text" name="_gotcha" tabindex="-1" autocomplete="off"></label>

      <button type="submit">Submit Application</button>
    </form>
  </div>
</div>

<!-- Success Message Overlay -->
<div id="successOverlay" class="success-overlay">
  <div class="success-content">
    <h3>✅ Application Received</h3>
    <p>Thank you for trusting Street Light to represent you. We’ll review your information and reach out soon to begin your personalized search.</p>
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
        alert("There was an issue submitting your application. Please try again.");
      }
    } catch {
      alert("Network error. Please try again later.");
    }
  });
});
</script>
