---
layout: service
title: Executive Strategy & Operations Coaching
tagline: An executive clarity session — strategy and focus in one hour.
price: "$100 / first hour — $60 each additional hour"
image: /assets/img/services/executive.webp
---

Executives and founders often operate at the edge of complexity — balancing growth, people, and purpose.  
This page helps you reset, refocus, and realign your strategy with clarity and conviction.

We’ll work together to:
- Refine your top strategic priorities  
- Identify operational and leadership bottlenecks  
- Establish measurable goals and accountability systems  
- Strengthen alignment between mission, metrics, and morale  

## Tags
Executive Coaching · Virtual COO · Business Strategy · Operations Consulting · Leadership Clarity

---

## Description
Are you a founder, executive director, or business owner who needs a trusted sounding board?  
This one-hour session offers **real-time clarity** for leaders navigating complex decisions.  
You’ll get focused, experienced guidance from a **Virtual COO** — your second-in-command for the hour.

## What’s Included
- 1-hour virtual strategy and operations call  
- Leadership, systems, and process review  
- Identification of current bottlenecks and blind spots  
- Quick wins and action steps summarized post-call  
- Optional extended session ($60/hour)

## Why It Works
- Outside perspective without long-term commitment  
- Clear, prioritized next steps after every session  
- Address systems, staff, and strategy in one integrated conversation

## Who This Is For
- Founders and executives seeking clarity  
- Nonprofit leaders managing growth or staff challenges  
- Business owners overwhelmed by operations  
- Teams facing communication or system breakdowns

---

<button id="startProcessBtn" class="btn">Start the Process</button>

<!-- Modal Overlay -->
<div id="formModal" class="form-modal">
  <div class="form-content">
    <button class="close-modal" aria-label="Close Form">&times;</button>
    <form action="https://formspree.io/f/mldpwzwy" method="POST" class="clarity-intake-form">
      <h3>Schedule an Executive Call</h3>
      <p>Use the form below to share what’s most important for us to focus on. Your responses remain confidential and are used only to tailor your session.</p>
      <p><em>“Plans fail for lack of counsel, but with many advisers they succeed.” — Proverbs 15:22</em></p>

      <label>Name:<br><input type="text" name="name" required></label><br>
      <label>Email:<br><input type="email" name="email" required></label><br>
      <label>Company/Organization:<br><input type="text" name="organization"></label><br>
      <label>Role/Title:<br><input type="text" name="role"></label><br>

      <label>1. What is your biggest current challenge as an executive/leader?<br>
        <textarea name="challenge" rows="3"></textarea>
      </label><br>

      <label>2. What do you most want to gain from this call?<br>
        <textarea name="goals" rows="3"></textarea>
      </label><br>

      <label>3. What would a successful outcome from this session look like to you?<br>
        <textarea name="success" rows="3"></textarea>
      </label><br>

      <fieldset>
        <legend>Preferred Call Length:</legend>
        <label><input type="radio" name="call_length" value="1 hour"> 1 Hour</label>
        <label><input type="radio" name="call_length" value="2 hours"> 2 Hours</label>
      </fieldset>

      <label>Preferred Call Date:<br><input type="date" id="preferred_date" name="preferred_date"></label><br>
      <label>Preferred Call Time:<br><input type="time" id="preferred_time" name="preferred_time"></label><br>

      <label>Time Zone:<br>
        <select id="time_zone" name="time_zone">
          <option value="">Please Select</option>
          <option value="Eastern Time (ET)">Eastern Time (ET)</option>
          <option value="Central Time (CT)">Central Time (CT)</option>
          <option value="Mountain Time (MT)">Mountain Time (MT)</option>
          <option value="Pacific Time (PT)">Pacific Time (PT)</option>
        </select>
      </label><br>

      <input type="hidden" id="user_timezone" name="user_timezone">
      <input type="hidden" id="converted_time_et" name="converted_time_et">

      <p class="disclaimer">
        <strong>Important Disclaimer:</strong><br>
        My coaching style incorporates biblical references as part of the process.  
        If this is not for you or makes you uncomfortable, please do not book the session.
      </p>

      <button type="submit">Submit Form</button>
    </form>
  </div>
</div>

<!-- Success Message Overlay -->
<div id="successOverlay" class="success-overlay">
  <div class="success-content">
    <h3>✅ Thanks!</h3>
    <p>Your form was submitted successfully. I’ll reach out soon to confirm your session.</p>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const startBtn = document.getElementById("startProcessBtn");
  const modal = document.getElementById("formModal");
  const closeBtn = modal.querySelector(".close-modal");
  const successOverlay = document.getElementById("successOverlay");
  const form = modal.querySelector("form");

  // Open modal
  startBtn.addEventListener("click", () => modal.classList.add("show"));

  // Close modal
  closeBtn.addEventListener("click", () => modal.classList.remove("show"));
  modal.addEventListener("click", (e) => {
    if (e.target === modal) modal.classList.remove("show");
  });

  // Handle form submission
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
        alert("There was an issue submitting the form. Please try again.");
      }
    } catch {
      alert("Network error. Please try again later.");
    }
  });

  // Detect user timezone
  const tzField = document.getElementById("user_timezone");
  if (tzField) tzField.value = Intl.DateTimeFormat().resolvedOptions().timeZone;
});
</script>
