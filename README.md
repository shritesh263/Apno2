# ApnoAI Internship Task 2 — Modern React Profile Card

A glassmorphism personal profile card built with **React 18 CDN**, **Tailwind CSS**, and **Babel Standalone** — running purely inside a single HTML file without any build configuration or `node_modules`.

Designed following modern 2026 UI aesthetics (Linear, Vercel, Stripe dashboards) with backdrop-blur glassmorphism, dynamic props, reactive state management, and an interactive appreciation counter.

---

## 🌟 Live Demo & Repository

> ### 🚀 **Live Demo:** [https://kpno20.vercel.app/](https://kpno20.vercel.app/)
> 
> 📦 **GitHub Repository:** [https://github.com/shritesh263/Apno2](https://github.com/shritesh263/Apno2)

[![Live Demo](https://img.shields.io/badge/Live_Demo-kpno20.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://kpno20.vercel.app/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Apno2-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shritesh263/Apno2)

---

## 🚀 Key Features

- **2026 Glassmorphism Aesthetic:** Layered translucent card with `backdrop-filter: blur(24px)`, subtle inner borders, ambient glowing radial mesh background, and micro-interactions.
- **Thinking in Components:** Structured into a clear component hierarchy (`App` ➔ `ProfileCard`).
- **Dynamic Props:** Personal information, avatar, role, bio, social links, projects, badges, and skills are passed into the component as pure, read-only props.
- **Reactive State (`useState` & `useEffect`):**
  - 🌓 **Dark Mode Toggle:** Seamless theme switching between dark and light modes.
  - ❤️ **Interactive Applaud / Like Counter (+10 XP Bonus):** Applaud button with dynamic counter state, toggle status, and **floating emoji particle burst** (`❤️`, `✨`, `🔥`, `👏`).
  - 🗂️ **Multi-Tab Switcher (`useState`):** Switch between **About**, **Projects** (interactive list), and **Badges** (highlights).
  - 🕒 **Live Local Clock (`useEffect`):** Real-time ticking Bengaluru time (`Asia/Kolkata`) updating every second with `setInterval` and cleanup.
  - 🔊 **Web Audio Micro-Chimes:** Synthesized interactive feedback chimes created on the fly with the Web Audio API, complete with a sound/mute toggle button.
  - 💬 **Quick Contact Modal Drawer:** Interactive glass modal to copy email or send a direct collaboration note.
  - 🔄 **Cyclical Status Picker:** Click the live status pill to cycle between custom availability statuses.
  - 🔗 **Share Profile Link:** One-click share button that copies the profile link to your clipboard with an animated floating toast banner.
  - 🏷️ **Interactive Skill Chips:** Click any skill chip to toggle and inspect active skills.

---

## 🧠 Core React Concepts: Props vs. State

| Concept | What It Is | How It's Used in this Project |
| :--- | :--- | :--- |
| **Props** (Properties) | **Inputs passed IN** to a component from its parent. Props are read-only and immutable. | `<ProfileCard name="Shritesh" role="Full-Stack Developer" skills={["React", ...]} />` |
| **State** (`useState`) | **Component Memory** that changes over time based on user interaction. Updating state causes React to re-render the UI. | `const [isDark, setIsDark] = useState(true);`<br>`const [likes, setLikes] = useState(142);` |

---

## 🤖 AI Debugging Reflection ("Explain, Don't Solve")

During development, intentional syntax break experiments were conducted to understand React runtime behavior:
- **Experiment:** Changing `useState` to `usestate` or misspelling JSX attributes.
- **Error in Console:** `TypeError: usestate is not a function` or uncaught Babel syntax error.
- **AI Explanation & Takeaway:** JavaScript and React hooks are strictly case-sensitive. React requires standard PascalCase/camelCase conventions (`useState`, `useEffect`) because Babel transpiles JSX into direct function calls (`React.createElement`). Understanding the underlying transpilation and hook rules empowers developers to diagnose console traces independently rather than relying on guesswork.

---

## 🛠️ How to Run Locally

Because this project runs with CDN dependencies, no build tools or package managers are required!

1. **Option 1: Direct Browser**
   - Double-click `index.html` to open it directly in Chrome, Edge, Brave, or Firefox.

2. **Option 2: Local HTTP Server (Recommended)**
   ```bash
   npx serve .
   # or
   python -m http.server 3000
   ```
   Open `http://localhost:3000` in your browser.

---

## 📦 Deployment to Vercel

1. Create a repository on GitHub named `Apno2`.
2. Push `index.html`, `profile.jpg`, and `README.md` to GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: add profile card component with props and state"
   git branch -M main
   git remote add origin https://github.com/shritesh263/Apno2.git
   git push -u origin main
   ```
3. Go to [vercel.com](https://vercel.com) ➔ **Add New Project** ➔ Import repository.
4. Framework Preset: **Other** (Static HTML).
5. Click **Deploy**. Your site is live at: **[https://kpno20.vercel.app/](https://kpno20.vercel.app/)**!
