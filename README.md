# Serene Minds

A beautiful, premium static HTML landing page for a psychology and mental wellness platform. **Find Your Inner Calm.**

This is the pure static version (single `index.html` + assets) — lightweight, zero dependencies, and ready to deploy instantly to GitHub Pages.

**Live Demo:** Deploy to GitHub Pages in under 2 minutes.

![Serene Minds](hero-bg.jpg)

## ✨ Features

- **Elegant, calming design** with premium typography (Playfair Display + Inter)
- Fully responsive (mobile, tablet, desktop)
- Interactive **Begin Your Journey** lead capture modal
- **4 beautiful article previews** with rich detail modals
- **8 Focus Areas** (Anxiety, Mindfulness, Emotional Intelligence, etc.)
- **Free Resources** section with interactive tools:
  - Guided breathing exercises (Box Breathing, 4-7-8, Physiological Sigh)
  - Journal prompts (downloadable)
  - Wellness worksheets
- Global **search modal** across topics & articles
- Smooth scroll navigation + mobile hamburger menu
- Scroll-triggered navbar effects
- Testimonials, stats, and compelling CTAs
- Zero build step — works directly in any browser

## 🚀 Quick Start (Local Development)

### Option 1: Open directly
```bash
# Just double-click index.html in your file explorer
```

### Option 2: Use a local server (recommended)

**Python (built-in):**
```bash
python -m http.server 8000
# Then open http://localhost:8000
```

**Node.js (http-server):**
```bash
npx http-server -p 8000 -c-1
```

**VS Code Live Server extension:**
Right-click `index.html` → "Open with Live Server"

## 📁 Project Structure

```
serene-minds/
├── index.html          # Main HTML (Tailwind via CDN + JS)
├── css/
│   └── styles.css      # All custom styles (extracted for maintainability)
├── logo1.jpg           # Brand logo (in root, next to index.html)
├── hero-bg.jpg         # Hero background
├── article1.jpg        # Article & testimonial images
├── article2.jpg
├── meditation.jpg
├── .github/
│   └── workflows/
│       └── deploy-pages.yml   # GitHub Pages deployment
├── .gitignore
├── .nojekyll           # Prevents Jekyll processing on GitHub Pages
├── LICENSE
└── README.md
```

## 🌐 Deploy to GitHub Pages (Automated)

This repo is pre-configured for zero-config deployment to GitHub Pages.

### One-time Setup

1. **Create a new GitHub repository**
   - Recommended name: `serene-minds`
   - Push this entire `serene-minds/` folder as the root of your repo

2. **Enable GitHub Pages**
   - Go to your repo → **Settings** → **Pages**
   - Under "Build and deployment" → **Source**: Select **GitHub Actions**

3. **Push your code**
   ```bash
   git add .
   git commit -m "Deploy Serene Minds"
   git push origin main
   ```

4. The included workflow will automatically deploy your site.

Your live site will be available at:
`https://<your-username>.github.io/serene-minds/`

### Troubleshooting Deployment

| Problem                    | Likely Cause                                      | Fix |
|---------------------------|---------------------------------------------------|-----|
| Images not showing        | Image paths in HTML don't match actual file locations | Keep images in root (next to index.html) and use paths like `logo1.jpg` |
| Site shows old version    | GitHub Pages still using "Deploy from a branch"   | Set Source to **GitHub Actions** in Settings → Pages |
| 404 on css/styles.css     | Workflow hasn't run yet                           | Go to **Actions** tab and wait for the workflow to complete |
| Changes not live          | Pushed to wrong branch                            | Always push to `main` branch |

**Pro tip**: After every push, go to the **Actions** tab to see the deployment progress.

## 🛠 Customization

| What you want to change       | Where to edit                  |
|-------------------------------|--------------------------------|
| Logo & hero images            | Root folder (same as index.html) |
| Colors & typography           | `css/styles.css` (CSS variables + custom classes) + Tailwind CDN |
| Content / copy                | Directly in `index.html`       |
| Add new articles              | Add to the articles grid + `articleData` array in `<script>` |
| Form submissions              | Replace `submitJourneyForm()` with your backend / Formspree / Netlify Forms |
| Add a contact page            | Create `contact.html` (keep same styling) |

All JavaScript is vanilla and contained in the single `<script>` tag at the bottom of `index.html`.

## 📄 Tech Stack

- **HTML5** + **CSS3** (Tailwind CSS via CDN)
- **Vanilla JavaScript** (no frameworks)
- **Font Awesome 6** (CDN icons)
- **Google Fonts** (Inter + Playfair Display)

**Total size:** ~150KB (mostly images) — extremely fast.

## 📝 Notes

- The site uses CDN links for Tailwind and Font Awesome. For maximum reliability in production you can self-host these assets later.
- All interactive features (modals, breathing animation, search, etc.) are fully functional without any backend.
- The "Begin Your Journey" form currently logs to console + shows success UI. Connect it to Resend, EmailJS, or a form service for production lead capture.

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

---

**Serene Minds** — A sanctuary for the mind. Compassionate guidance for those ready to heal.

*Find Your Inner Calm.*
