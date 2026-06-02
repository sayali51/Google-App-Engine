# 🚀 Personal Portfolio — Deployed on Google App Engine

A clean, responsive personal portfolio website built with HTML & CSS and deployed to **Google Cloud App Engine**.

🔗 **Live Site:** [https://practice-495611.el.r.appspot.com/](https://practice-495611.el.r.appspot.com/)

---

## 📋 About

This is a single-page portfolio website for **Sayali Anil Kale**, a 3rd-year B.Tech Computer Science student from Pune, India. The site showcases her background, interests, and academic journey, and serves as a hands-on project for learning cloud deployment using Google App Engine.

---

## 🗂️ Project Structure

```
Google-App-Engine/
├── index.html      # Main portfolio page (HTML + CSS + animations)
├── app.yaml        # Google App Engine configuration
└── README.md       # Project documentation
```

---

## ✨ Features

- **Responsive design** — works across desktop and mobile
- **Smooth animations** — fade-up entrances and floating background elements
- **Fixed navigation** with glassmorphism blur effect
- **Hero section** with animated gradient circles
- **About section** with a two-column info card layout
- **Education section** with a hover-interactive card
- Custom purple design system using CSS variables
- Google Fonts: *DM Serif Display* & *DM Sans*

---

## ⚙️ App Engine Configuration (`app.yaml`)

```yaml
runtime: python311
env: standard
instance_class: F1

handlers:
  - url: /
    static_files: index.html
    upload: index.html
  - url: /.*
    static_files: index.html
    upload: index.html

automatic_scaling:
  min_idle_instances: automatic
  max_idle_instances: automatic
  max_instances: 5
```

The app runs on the **Python 3.11 standard environment** and serves `index.html` as a static file for all routes. Automatic scaling is enabled with a cap of 5 instances.

---

## 🛠️ Deployment

### Prerequisites

- [Google Cloud SDK](https://cloud.google.com/sdk/docs/install) installed
- A Google Cloud project with billing enabled
- App Engine API enabled for your project

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/sayali51/Google-App-Engine.git
cd Google-App-Engine

# 2. Authenticate with Google Cloud
gcloud auth login

# 3. Set your project ID
gcloud config set project YOUR_PROJECT_ID

# 4. Deploy to App Engine
gcloud app deploy

# 5. Open the live app
gcloud app browse
```

---

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 / CSS3 | Frontend structure and styling |
| CSS Variables | Design token system |
| Google Fonts | Typography (DM Serif Display, DM Sans) |
| Google App Engine | Cloud hosting & deployment |
| `app.yaml` | GAE runtime and routing configuration |

---


## 📄 License

This project is open source and available for learning and reference purposes.
