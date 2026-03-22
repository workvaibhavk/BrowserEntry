# 🌐 Browser Entry Page

> *"Sleep less, Code more"*

A clean, minimal, and fully personalized browser start page — built with pure HTML, Tailwind CSS, and vanilla JavaScript. Designed to replace your default new tab with something actually useful: quick access to your tools, projects, AI agents, documentation, and more — all in one place.

🔗 **Live Demo:** [workvaibhavk.github.io/BrowserEntry](https://workvaibhavk.github.io/BrowserEntry/)

---

## 📸 Preview

> Open the live link above to see it in action.  
> The page greets you with a real-time clock, profile section, sidebar shortcuts, and categorized link cards.

---

## ✨ Features

- **Live Clock** — Displays current time in 24-hour format, updated every 55 seconds automatically.
- **Sidebar Quick Links** — One-click access to Vercel, Supabase, Clerk, Lucide Icons, Google Fonts, and personal projects.
- **Profile Section** — Hover on your profile image for a fun swap effect.
- **Categorized Link Cards** — Organized sections for Professional, AI Agents, and Documentation links.
- **Design Tools Drawer** — A hover-triggered floating panel with links to Canva, Figma, Dribbble, Pinterest, and Excalidraw.
- **Tooltip Support** — Custom CSS tooltips on every icon for clean UX.
- **Gradient Background** — Soft warm-to-cool gradient for an easy-on-the-eyes aesthetic.
- **Fully Static** — No frameworks, no build step, no dependencies to install. Just open and go.
- **Responsive Layout** — Built with Tailwind utility classes for flexible layout.

---

## 🗂️ Project Structure

```
BrowserEntry/
├── index.html          # Main HTML structure and layout
├── style.css           # Custom CSS (tooltips, sidebar, cards, gradients)
├── script.js           # Vanilla JS (show, hide, updateTime functions)
├── me.png              # Your profile picture (default state)
├── notme.png           # Profile picture on hover (fun swap)
└── svg/                # All icons and images
    ...
```

---

## ⚙️ Installation / Setup

### Option 1 — Use it directly (Live)

Just visit: [https://workvaibhavk.github.io/BrowserEntry/](https://workvaibhavk.github.io/BrowserEntry/)

---

### Option 2 — Run Locally

**Step 1: Clone the repository**
```bash
git clone https://github.com/workvaibhavk/BrowserEntry.git
```

**Step 2: Navigate into the project folder**
```bash
cd BrowserEntry
```

**Step 3: Add your assets**  
Place all your icons and images inside the `svg/` folder as referenced in `index.html`. Replace `me.png` and `notme.png` with your own profile pictures.

**Step 4: Open in browser**  
Just double-click `index.html` or open it via your browser:
```
File → Open File → index.html
```
No server, no npm install, no build step required.

---

### Option 3 — Set as Browser Start Page

**Chrome:**
1. Go to `Settings`
2. Under **On startup**, select **Open a specific page or set of pages**
3. Click **Add a new page**
4. Paste: `https://workvaibhavk.github.io/BrowserEntry/`

**Firefox:**
1. Go to `Settings → Home`
2. Set **Homepage and new windows** to **Custom URLs**
3. Paste: `https://workvaibhavk.github.io/BrowserEntry/`

**Edge:**
1. Go to `Settings → Start, home, and new tabs`
2. Under **When Edge starts**, choose **Open these pages**
3. Add the URL

---

## 🧠 How It Works

### updateTime()
Reads the current system time and displays it in 24-hour format inside the #time element in the sidebar. Called once on page load via window.onload, then re-calls itself every 55 seconds using setInterval.

### show()
Triggered on onmouseover of the floating design tools button. Removes the hidden class and adds flex to the #drag element, making the drawer visible.

### hide()
Triggered on onmouseout. Reverses the action — removes flex and adds hidden back to collapse the drawer.

### Profile Image Swap
The <img> tag for the profile photo uses inline onmouseover and onmouseleave to swap between me.png and notme.png for a fun hover effect.

### Tooltip System
Tooltips are built entirely in CSS using the ::after pseudo-element on .tooltip class, reading the label from the data-tip attribute. No JavaScript needed.

---

## 🛠️ Built With

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and layout |
| [Tailwind CSS (Browser CDN)](https://tailwindcss.com) | Utility-first styling |
| CSS3 | Custom styles, tooltips, gradients |
| Vanilla JavaScript | Clock, drawer toggle |
| GitHub Pages | Hosting and deployment |

---

## 🔧 Customization Guide

Want to make it your own? Here's what to change:

- *Profile image* — Replace me.png and notme.png with your photos.
- *Sidebar links* — Edit the <a> tags inside .sidebar in index.html.
- *Cards* — Add or remove link entries inside the Professional, AI Agents, or Documentation cards.
- *Quote* — Find "Sleep less, Code more" in index.html and replace with your own.
- *Background* — In style.css, change the background-image gradient values on body.
- *Clock update interval* — In script.js, change 55000 in setInterval(updateTime, 55000) to your preferred ms value.

---
## 🤝 Contributing

Contributions are welcome! Follow the steps below to go from *Fork* to *Pull Request*.

---

### Step 1 — Fork the Repository

1. Go to the repository: [github.com/workvaibhavk/BrowserEntry](https://github.com/workvaibhavk/BrowserEntry)
2. Click the *Fork* button at the top-right corner of the page.
3. This creates a copy of the repository under your own GitHub account.

---

### Step 2 — Clone Your Fork

bash
git clone https://github.com/<your-username>/BrowserEntry.git
cd BrowserEntry


Replace <your-username> with your actual GitHub username.

---

### Step 3 — Create a New Branch

Always create a new branch for your changes. Never work directly on main.

bash
git checkout -b feature/your-feature-name


Example:
bash
git checkout -b feature/add-dark-mode


---

### Step 4 — Make Your Changes

Edit the files as needed:
- index.html for layout or link changes
- style.css for styling changes
- script.js for JavaScript logic changes
- svg/ folder for new icons or images

---

### Step 5 — Stage and Commit Your Changes

bash
git add .
git commit -m "feat: describe what you changed"


Use clear, short commit messages. Examples:
- feat: add dark mode toggle
- fix: tooltip alignment on mobile
- chore: update sidebar icons

---

### Step 6 — Push to Your Fork

bash
git push origin feature/your-feature-name


---

### Step 7 — Open a Pull Request

1. Go to your forked repo on GitHub: github.com/<your-username>/BrowserEntry
2. You'll see a banner saying *"Compare & pull request"* — click it.
3. Make sure the base repository is set to workvaibhavk/BrowserEntry and base branch is main.
4. Add a clear *title* and *description* explaining what your PR does.
5. Click *"Create pull request"* — done! 🎉

---

### Step 8 — Wait for Review

The maintainer will review your PR. You may be asked to make changes. If so:
1. Make the requested edits locally
2. Commit and push to the same branch
3. The PR will update automatically

---

### ✅ Contribution Guidelines

- Keep changes focused — one feature or fix per PR.
- Do not commit unnecessary files (.DS_Store, node_modules, etc.).
- Test your changes locally before submitting.
- Be respectful and constructive in all discussions.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

*Vaibhav K*  
GitHub: [@workvaibhavk](https://github.com/workvaibhavk)  
Team: [Team Crazxy](https://github.com/Teamcrazxy/)

---

## 🌟 Show Your Support

If you like this project, consider giving it a ⭐ on GitHub — it helps a lot!

---

Built with ☕ and the motto: "Sleep less, Code more"