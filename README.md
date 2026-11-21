
<h1 align="center">Hi 👋, I'm Durgesh Gosavi</h1>

<h3 align="center">🚀 Full Stack Developer | Web Developer</h3>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=500&size=22&duration=3000&pause=1000&color=00F7FF&center=true&vCenter=true&width=650&lines=Full+Stack+Developer;Frontend+%7C+Backend+Developer;React+%7C+JavaScript+%7C+Node.js;Building+Modern+Web+Applications;Code.+Create.+Innovate." />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=YOUR_USERNAME&label=Profile%20Views&color=00ffff&style=for-the-badge" />
</p>

---

## 👨‍💻 About Me

- 🚀 I'm a passionate Full Stack Developer.
- 💻 Interested in Frontend and Backend Development.
- 🌱 Currently learning and exploring modern web technologies.
- 🔭 Building responsive and user-friendly web applications.
- 🧠 Love solving problems and learning new technologies.
- 🎯 Goal: To become an expert Full Stack Developer.
- ⚡ Fun fact: I turn coffee ☕ into code!

---

## 🛠️ Tech Stack & Tools

### 🎨 Frontend Development
<p>
  <img src="https://skillicons.dev/icons?i=html,css,js,react,bootstrap" />
</p>

### ⚙️ Backend Development
<p>
  <img src="https://skillicons.dev/icons?i=nodejs,express,python,cs" />
</p>

### 🗄️ Database
<p>
  <img src="https://skillicons.dev/icons?i=mongodb,mysql" />
</p>

### 🔧 Tools & Technologies
<p>
  <img src="https://skillicons.dev/icons?i=git,github,vscode,postman,npm" />
</p>

---

## 📊 GitHub Statistics

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=tokyonight&hide_border=true" />
</p>

---

## 🔥 GitHub Contribution Streak

<p align="center">
  <img src="https://streak-stats.demolab.com?user=YOUR_USERNAME&theme=tokyonight&hide_border=true" />
</p>

---

## 🐍 Watch My Contributions Get Eaten!

<p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake-dark.svg" />
</p>

---

## 📈 Contribution Activity

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&theme=tokyo-night&hide_border=true&area=true" />
</p>

---

## 🌐 Connect With Me

<p align="center">
  <a href="https://linkedin.com/in/YOUR_LINKEDIN">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://github.com/YOUR_USERNAME">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</p>

---

<h3 align="center">💻 Code | Create | Connect | Repeat</h3>

<p align="center">
  ⭐ Thanks for visiting my profile!
</p>


name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest

    permissions:
      contents: write

    steps:
      - name: Generate contribution snake
        uses: Platane/snk@v3
        with:
          github_user_name: YOUR_USERNAME
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push snake animation
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
