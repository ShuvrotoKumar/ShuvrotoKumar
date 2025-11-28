<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Stars Animation</title>

<style>
  body {
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: radial-gradient(ellipse at bottom, #0d1d31 0%, #0c0d13 100%);
    overflow: hidden;
  }

  .stars {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 120%;
    transform: rotate(-45deg);
  }

  .star {
    --star-color: #4fc3f7;
    --star-tail-length: 6em;
    --star-tail-height: 2px;
    --star-width: calc(var(--star-tail-length) / 6);

    position: absolute;
    width: var(--star-tail-length);
    height: var(--star-tail-height);
    background: linear-gradient(45deg, currentColor, transparent);
    color: var(--star-color);
    border-radius: 50%;
    filter: drop-shadow(0 0 6px currentColor);

    animation: fall linear infinite, tail-fade ease-out infinite;
    transform: translate3d(100vw, 0, 0);
  }

  .star::before,
  .star::after {
    content: "";
    position: absolute;
    left: calc(var(--star-width) / -2);
    width: var(--star-width);
    height: 100%;
    border-radius: inherit;
    background: linear-gradient(45deg, transparent, currentColor, transparent);
    animation: blink 2s linear infinite;
  }

  .star::before { transform: rotate(45deg); }
  .star::after { transform: rotate(-45deg); }

  @keyframes fall {
    to {
      transform: translate3d(-30em, 0, 0);
    }
  }

  @keyframes tail-fade {
    0%, 50% {
      width: var(--star-tail-length);
      opacity: 1;
    }
    70%, 80% {
      width: 0;
      opacity: 0.4;
    }
    100% {
      width: 0;
      opacity: 0;
    }
  }

  @keyframes blink {
    50% {
      opacity: 0.6;
    }
  }

  /* Random star positions + timings */
</style>

<script>
  // Generate stars dynamically (same SCSS logic but in JS)
  document.addEventListener("DOMContentLoaded", () => {
    const starContainer = document.querySelector(".stars");

    const starCount = 50;

    for (let i = 0; i < starCount; i++) {
      const star = document.createElement("div");
      star.className = "star";

      const tailLength = (Math.random() * (7.5 - 5) + 5).toFixed(2) + "em";
      const topOffset = Math.random() * 100 + "vh";
      const fallDuration = (Math.random() * (12 - 6) + 6).toFixed(2) + "s";
      const fallDelay = (Math.random() * 10).toFixed(2) + "s";

      star.style.setProperty("--star-tail-length", tailLength);
      star.style.setProperty("--top-offset", topOffset);
      star.style.setProperty("top", topOffset);
      star.style.animationDuration = `${fallDuration}, ${fallDuration}`;
      star.style.animationDelay = `${fallDelay}, ${fallDelay}`;

      starContainer.appendChild(star);
    }
  });
</script>

</head>

<body>
  <div class="stars"></div>
</body>

</html>

<!-- HEADER ANIMATION -->
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&size=22&pause=1000&color=4B9CE2&center=true&vCenter=true&width=700&lines=Hi%2C+I'm+Shuvroto+Kumar+👋;Frontend+Developer+(React+%26+Next.js);I+Love+Creating+Smooth+%26+Modern+Web+Experiences" />
</p>

---

<!-- ABOUT -->
## 👨‍💻 About Me
- 🚀 Frontend Developer specializing in **React**, **Next.js**, **Tailwind**, and **Ant Design**  
- 🎨 Passionate about clean UI, animations, and smooth user experience  
- 🔍 Focused on writing optimized & maintainable code  
- 📚 Always learning & exploring new web technologies  

---

<!-- TECH STACK -->
## ⚡ Tech Stack
<p align="left">
  <img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,js,ts,html,css,git,github,vscode" />
</p>

---

<!-- PORTFOLIO -->
## 🌐 Portfolio  
🔗 **Live Portfolio:** _[Add your portfolio link here]_  

---

<!-- PROJECTS -->
## 🔥 Featured Projects
Here are some of my highlighted works:

### 🚀 **Project 1: Next.js Modern Landing Page**
- ⚙️ Tech: Next.js, Tailwind CSS
- 🔗 Live: furniture-landing-ppz8.vercel.app


### 📊 **Project 2: CRM Dashboard (Next.js + Ant Design)**
- Interactive tables, charts, sidebar, role management  
- 🔗 Live: crm-dashboard-bice.vercel.app

### 🎧 **Project 3: Music Copyright Detection Web App**
- MERN + React UI  
- 🔗 Live: add link

Add as many projects as you want.

---

<!-- STATS -->
## 📊 GitHub Stats
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ShuvrotoKumar&show_icons=true&theme=tokyonight" height="160" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=ShuvrotoKumar&theme=tokyonight" height="160" />
</p>

---

<!-- BADGES -->
## 🧩 Profile Insights  
![Profile Views](https://komarev.com/ghpvc/?username=ShuvrotoKumar&style=flat-square&color=blue)

---

<!-- SOCIALS -->
## 📬 Connect With Me  
Replace these with your real social links:

[![LinkedIn](https://skillicons.dev/icons?i=linkedin)](https://linkedin.com/)
[![Facebook](https://skillicons.dev/icons?i=facebook)](https://facebook.com/)
[![Gmail](https://skillicons.dev/icons?i=gmail)](mailto:sdks6409@gmail.com)

---

<p align="center">
  Thanks for visiting my GitHub profile! 🌟  
</p>
