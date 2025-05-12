
# 🌐 Md. Naib Hossain Khan — Developer Portfolio

Welcome to my personal portfolio site built with [Hugo](https://gohugo.io/) and powered by the minimalist [hugo-porto](https://themes.gohugo.io/themes/hugo-porto/) theme. This site showcases my work, skills, and experience in software engineering, specializing in full-stack development, backend architecture, and scalable microservices.

---

## 🛠️ Tech Stack

- **Static Site Generator:** [Hugo](https://gohugo.io/)
- **Theme:** [hugo-porto](https://themes.gohugo.io/themes/hugo-porto/)
- **Hosting:** GitHub Pages
- **CI/CD:** Manual (via `gh-pages` branch)

---

## 🚀 Quick Start

### 1. Clone this repo

```bash
git clone https://github.com/naib77/naib-porto.git
cd naib-porto
```

### 2. Install Hugo

Follow the official instructions here:  
👉 https://gohugo.io/installation/

### 3. Create your Hugo site

```bash
hugo new site naib-porto
cd naib-porto
git init
git submodule add https://github.com/angelodlfrtr/hugo-porto.git themes/porto
```

### 4. Set up `config.toml`

```toml
baseURL = "https://naib77.github.io/naib-porto/"
languageCode = "en-us"
title = "Md. Naib Hossain Khan"
theme = "porto"
disableKinds = ["taxonomy", "term"]

[params]
  name = "Md. Naib Hossain Khan"
  tagline = "Sr. Software Engineer | Full Stack Developer"
  email = "knaib19@gmail.com"
  github = "https://github.com/naib77"
  linkedin = "https://t.ly/z6Iu"
  avatar = "images/profile.jpg"
  description = "I am a seasoned developer with 8+ years of experience in Java, Spring Boot, Angular, React, Kafka, and microservices."

[[params.projects]]
  name = "Agroshift Sera App"
  url = "#"
  description = "Designed and developed scalable backend/frontend architecture for Agroshift."

[[params.projects]]
  name = "Mfi Identity Service"
  url = "#"
  description = "Implemented reactive microservices using WebFlux, Kafka, PostgreSQL."

[[params.projects]]
  name = "Smart Vending Platform"
  url = "#"
  description = "Built ReactJS + Spring Boot app for gas meter integration."
```

### 5. Add Profile Image

Place your profile picture at:
```
static/images/profile.jpg
```

---

## 📝 Content Structure

Create basic pages:

```bash
mkdir -p content
cat <<EOT > content/_index.md
---
title: "Home"
---
Welcome to my portfolio.
EOT
```

To add specific sections:

```bash
hugo new about/index.md
hugo new projects/index.md
hugo new experience/index.md
hugo new education/index.md
hugo new contact/index.md
```

---

## 💻 Run Locally

```bash
hugo server -D --baseURL=http://localhost:1313/
```

Open your browser at: [http://localhost:1313](http://localhost:1313)

---

## 🏗️ Build & Deploy

```bash
rm -rf public
hugo --minify --cleanDestinationDir

cd public
git init
git checkout -b gh-pages
git remote add origin https://github.com/naib77/naib-porto.git
git add .
git commit -m "Deploy hugo-porto portfolio"
git push -u origin gh-pages --force

# Optional: commit submodule
cd ..
git submodule add git@github.com:naib77/naib-porto.git public
git add .
git commit -m "Deploy hugo-porto portfolio"
git push -u origin main --force
```

---

## 🙋‍♂️ About Me

📫 [LinkedIn](https://t.ly/z6Iu) | [GitHub](https://github.com/naib77) | ✉️ knaib19@gmail.com

---

> © 2025 Md. Naib Hossain Khan. Powered by Hugo & GitHub Pages.
