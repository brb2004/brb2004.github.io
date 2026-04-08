# Professional Online Portfolio — Setup Guide

## Files in this folder

```
portfolio/
├── index.html       ← Home page (start here)
├── about.html       ← About Me page
├── projects.html    ← Projects + AI Bot coming soon card
├── resume.html      ← Resume with PDF embed
├── contact.html     ← Contact page
├── style.css        ← All styling (don't rename this)
├── resume.pdf       ← YOUR RESUME — add this file
└── README.md        ← This file
```

---

## Quick setup checklist

### 1. Replace "Your Name" in every file
Search for `Your Name` across all .html files and replace with your actual name.

### 2. Add your photo
- On `index.html`: find the `photo-placeholder` div → replace with:
  ```html
  <img src="photo.jpg" alt="Your Name smiling" style="width:100%;height:100%;object-fit:cover;">
  ```
- On `about.html`: same — find `about-photo` div → replace with an `<img>` tag.

### 3. Add your video intro (index.html)
Inside the `video-embed-area` div, replace the placeholder with a YouTube embed:
```html
<iframe width="100%" height="100%"
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
  frameborder="0" allowfullscreen style="border-radius:6px;"></iframe>
```

### 4. Add your resume PDF (resume.html)
- Save your resume as `resume.pdf` in this folder.
- In `resume.html`, find the `resume-iframe-placeholder` div and replace it with:
```html
<iframe src="resume.pdf" width="100%" height="700px"
  style="border:none;" title="Resume PDF">
  <p>Your browser doesn't support PDF embeds.
     <a href="resume.pdf">Download the PDF</a> instead.</p>
</iframe>
```

### 5. Fill in your content (all pages)
- `about.html` — replace placeholder text with your actual story, interests, goals
- `projects.html` — embed your 3 projects (see inline comments for how)
- `contact.html` — replace `your.email@example.com` and LinkedIn URL
- Update all footer copyright lines with your name

### 6. Fill in the "At a Glance" cards (resume.html)
Replace the placeholder university, major, GPA, and skills with your real info.

---

## Hosting options (free)

| Platform | How | Notes |
|---|---|---|
| **GitHub Pages** | Push folder to a repo, enable Pages in Settings | Free, reliable, custom domain supported |
| **Netlify** | Drag and drop the folder at netlify.com/drop | Instant, free, HTTPS included |
| **Vercel** | Connect GitHub repo | Fast deploys on every push |

All three are completely free for a static site like this.

---

## Adding the AI Chatbot later

When your RAG server is ready, open `projects.html` and:

1. Delete the `<div class="coming-soon-card">...</div>` block
2. Uncomment the `CHATBOT SLOT` comment block below it
3. Point the `<iframe src="">` at your hosted chatbot URL

That's it — the rest of the page stays exactly the same.

---

## Customization tips

- **Colors**: open `style.css`, look for `:root { ... }` at the top. Change `--accent` for a different highlight color.
- **Fonts**: the Google Fonts import at the top of style.css loads Cormorant Garamond + DM Sans. Swap for any Google Font pair you prefer.
- **Nav name**: change `Your Name` in the `nav-brand` anchor on each page.
