---
layout: page
title: "Executive Strategy"
permalink: /executive-strategy/
---

# Executive Strategy & Clarity

Executives and founders often operate at the edge of complexity — balancing growth, people, and purpose.  
This page helps you reset, refocus, and realign your strategy with clarity and conviction.

We’ll work together to:
- Refine your top strategic priorities  
- Identify operational and leadership bottlenecks  
- Establish measurable goals and accountability systems  
- Strengthen alignment between mission, metrics, and morale  

---

## Schedule an Executive Clarity Call

Use the form below to share what’s most important for us to focus on.  
Your responses remain confidential and are used only to tailor your session.

<form action="https://formspree.io/f/mldpwzwy" method="POST" class="clarity-intake-form">
  <h3>Executive Clarity Call – Intake Form</h3>
  <p><em>“Plans fail for lack of counsel, but with many advisers they succeed.” — Proverbs 15:22</em></p>

  <label>Name:<br><input type="text" name="name" required></label><br>
  <label>Email:<br><input type="email" name="email" required></label><br>
  <label>Company/Organization:<br><input type="text" name="organization"></label><br>
  <label>Role/Title:<br><input type="text" name="role"></label><br>
  <label>Phone (optional):<br><input type="tel" name="phone"></label><br>

  <label>1. What is your biggest current challenge as an executive/leader?<br>
    <textarea name="challenge" rows="3"></textarea>
  </label><br>

  <label>2. What do you most want to gain from this call?<br>
    <textarea name="goals" rows="3"></textarea>
  </label><br>

  <label>3. What would a successful outcome from this session look like to you?<br>
    <textarea name="success" rows="3"></textarea>
  </label><br>

  <label>4. Are there any sensitive topics you’d like handled with extra care?<br>
    <textarea name="sensitive" rows="3"></textarea>
  </label><br>

  <label>5. On a scale of 1–10, how clear do you currently feel about your direction?<br>
    <input type="range" name="clarity" min="1" max="10" value="5">
  </label><br>

  <label>6. What are your top 3 priorities for your organization in the next 6–12 months?<br>
    <textarea name="priorities" rows="3"></textarea>
  </label><br>

  <label>7. If you were to move forward with regular coaching, what would success look like after 3 months?<br>
    <textarea name="coaching_success" rows="3"></textarea>
  </label><br>

  <fieldset>
    <legend>Preferred Call Length:</legend>
    <label><input type="radio" name="call_length" value="1 hour"> 1 Hour</label>
    <label><input type="radio" name="call_length" value="2 hours"> 2 Hours</label>
  </fieldset>

  <fieldset>
    <legend>Would you be open to regular coaching sessions?</legend>
    <label><input type="radio" name="regular_sessions" value="Yes"> Yes</label>
    <label><input type="radio" name="regular_sessions" value="No"> No</label>
  </fieldset>

  <fieldset>
    <legend>If yes, what frequency would you prefer?</legend>
    <label><input type="radio" name="frequency" value="Weekly"> Weekly</label>
    <label><input type="radio" name="frequency" value="Bi-Weekly"> Bi-Weekly</label>
    <label><input type="radio" name="frequency" value="Monthly"> Monthly</label>
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
      <option value="Alaska Time (AKT)">Alaska Time (AKT)</option>
      <option value="Hawaii Time (HST)">Hawaii Time (HST)</option>
      <option value="Other / International">Other / International</option>
    </select>
  </label><br>

  <input type="hidden" id="user_timezone" name="user_timezone">
  <input type="hidden" id="converted_time_et" name="converted_time_et">

  <!-- Honeypot for spam prevention -->
  <input type="text" name="_gotcha" style="display:none" tabindex="-1" autocomplete="off">

  <label>How confident are you in your current leadership team’s alignment (1–10)?<br>
    <input type="range" name="team_alignment" min="1" max="10" value="5">
  </label><br>

  <p class="disclaimer">
    <strong>Important Disclaimer:</strong><br>
    My coaching style incorporates biblical references as part of the process.  
    If this is not for you or makes you uncomfortable, please do not book the session.  
    This form is confidential and designed to help us make the most of our time together.
  </p>

  <button type="submit">Submit Form</button>
</form>

<script>
document.addEventListener("DOMContentLoaded", () => {
  // Detect user's time zone
  const userTZ = Intl.DateTimeFormat().resolvedOptions().timeZone;
  document.getElementById("user_timezone").value = userTZ;

  // Map for common U.S. zones
  const map = {
    "America/New_York": "Eastern Time (ET)",
    "America/Chicago": "Central Time (CT)",
    "America/Denver": "Mountain Time (MT)",
    "America/Los_Angeles": "Pacific Time (PT)",
    "America/Anchorage": "Alaska Time (AKT)",
    "Pacific/Honolulu": "Hawaii Time (HST)"
  };
  if (map[userTZ]) {
    document.getElementById("time_zone").value = map[userTZ];
  }

  // Convert to ET before submission
  const form = document.querySelector(".clarity-intake-form");
  form.addEventListener("submit", () => {
    const date = document.getElementById("preferred_date").value;
    const time = document.getElementById("preferred_time").value;
    if (date && time) {
      const localDateTime = new Date(`${date}T${time}`);
      const etDateTime = new Date(localDateTime.toLocaleString("en-US", { timeZone: "America/New_York" }));
      document.getElementById("converted_time_et").value = etDateTime.toISOString();
    }
  });
});
</script>

---

<style>
.clarity-intake-form {
  background: #fafafa;
  padding: 1.5rem;
  border-radius: 8px;
  border: 1px solid #ddd;
  max-width: 650px;
  margin: 2rem auto;
  font-family: "Inter", sans-serif;
}
.clarity-intake-form input,
.clarity-intake-form textarea,
.clarity-intake-form select {
  width: 100%;
  margin-bottom: .8rem;
  padding: .4rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}
.clarity-intake-form fieldset {
  border: none;
  margin-bottom: 1rem;
}
.clarity-intake-form legend {
  font-weight: 600;
  margin-bottom: .3rem;
}
.clarity-intake-form button {
  background: #004aad;
  color: #fff;
  padding: .6rem 1.2rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.clarity-intake-form button:hover {
  background: #00337a;
}
.disclaimer {
  font-size: .9rem;
  color: #333;
  border-top: 1px solid #eee;
  padding-top: 1rem;
}
</style>
