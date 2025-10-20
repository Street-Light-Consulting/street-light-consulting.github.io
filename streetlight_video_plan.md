# 🎬 Street Light Consulting Video Plan
**Prepared by:** Rob Street  
**Date:** October 2025  

---

## 1. Purpose and Vision
The video component of *Street Light Consulting* will visually extend the message of the podcast — **The Science of Joy** — combining short reflections on leadership, neuroscience, and faith with a calm, branded presentation.

Videos will complement the audio podcast, enhance website engagement, and serve as visual devotionals for leaders seeking renewal.

---

## 2. Objectives
- Create short (3–8 minute) visual reflections aligned with each podcast episode.  
- Maintain complete control over hosting, branding, and playback environment.  
- Ensure videos are ad-free, distraction-free, and consistent with the Street Light aesthetic.  
- Provide a scalable foundation for future workshops, video courses, and client sessions.

---

## 3. Platform Selection
### ✅ **Chosen Platform: Cloudflare Stream**
- **Reason:** Professional, secure, self-hosted experience that integrates seamlessly with the Jekyll-based website.  
- **Billing Model:** Pay-per-minute for storage and delivery (cost-efficient for a small catalog).  
- **Core Benefits:**
  - Ad-free playback under the `streetlight.consulting` domain.  
  - Customizable, brand-aligned player.  
  - Automatic encoding for all devices (desktop, tablet, mobile).  
  - Optional domain restrictions for client-only access.

---

## 4. Workflow Overview
1. Record and edit video reflections (MP4 format).  
2. Upload to **Cloudflare Stream**.  
3. Copy the **embed code** from Cloudflare.  
4. Insert it into the podcast episode’s Markdown front matter as `video_embed`.  
5. The Jekyll layout (`podcast.html`) renders it automatically using a simple include.

---

## 5. Example Integration
**Front Matter (Markdown):**
```yaml
---
title: "Episode 1 – The Science of Joy"
date: 2025-10-16
video_embed: >
  <iframe src="https://iframe.videodelivery.net/your-video-id"
  width="640" height="360" frameborder="0"
  allow="accelerometer; autoplay; encrypted-media; picture-in-picture;"
  allowfullscreen></iframe>
---
```

**In your Jekyll Layout:**
```liquid
{% if page.video_embed %}
  <div class="video-container">
    {{ page.video_embed }}
  </div>
{% endif %}
```

**Recommended CSS:**
```css
.video-container iframe {
  width: 100%;
  max-width: 800px;
  height: auto;
  aspect-ratio: 16 / 9;
  display: block;
  margin: 2rem auto;
  border-radius: 8px;
}
```

---

## 6. Branding & Design
- **Visual Style:** Calm, minimal, reflective — soft gold, navy, and ivory palette.  
- **Lighting:** Natural or warm studio lighting; avoid harsh shadows.  
- **Intro/Outro:** 5-second fade with logo and soft piano cue.  
- **Font Overlay:** Use clean sans-serif typography for quotes or titles (e.g., Lato, Open Sans).  
- **Watermark:** Optional “Street Light” logo in lower-right corner for brand continuity.

---

## 7. Security & Privacy
- Enable **domain-restricted playback** (`streetlight.consulting`) in Cloudflare Stream.  
- For private client videos, use **Signed URLs** or “Direct URL Only” mode.  
- Do not expose raw MP4 links; always embed through Cloudflare’s secure player.

---

## 8. Publishing Schedule
- Publish one video per podcast episode (every Friday).  
- Upload to Cloudflare Stream by Wednesday to allow encoding and testing.  
- Embed on episode page and promote across:
  - LinkedIn post with clip snippet (under 1 minute).  
  - Street Light Consulting blog.  
  - Optional YouTube “short” version linking back to the full episode on the website.

---

## 9. Future Development
- Expand into **video devotionals** (60–90 second reflections).  
- Create a **Video Workshop Series** companion to consulting programs.  
- Add subtitle support for accessibility (via `.vtt` caption files).  
- Develop a **Video Archive** page categorized by theme (e.g., Joy, Leadership, Renewal).

---

## 10. Mission Statement
> *“To bring light to leadership through visuals that reflect peace, purpose, and divine design.”*
