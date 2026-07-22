# Corevo Interior Landing Page

A refined, lightweight, and responsive landing page for **Corevo Interior** — renovation and interior design partner in Malaysia.

This project is organized as a clean, static website structure ready for direct publication on **GitHub Pages**, **Vercel**, **Netlify**, or standard web servers.

---

## 📂 Folder Structure

```text
project-root/
├── index.html              # Main static homepage
├── README.md               # Project documentation guide
├── LICENSE                 # MIT License file
├── .gitignore              # Git ignore rules
└── assets/                 # Website static assets
    ├── css/
    │   └── style.css       # Production compiled CSS stylesheet
    ├── scss/
    │   └── style.scss      # Optional SASS/SCSS source stylesheet
    ├── js/
    │   └── main.js         # Interactive JavaScript engine
    ├── images/             # All local web-optimized image files
    │   ├── hero-banner.png
    │   ├── solution-design.png
    │   ├── solution-budget.png
    │   ├── solution-project.png
    │   ├── portfolio-living-room.png
    │   ├── portfolio-kitchen.png
    │   ├── portfolio-bedroom.png
    │   └── portfolio-dining.jpeg
    └── webfonts/           # Webfonts directory for custom font files (.woff, .woff2)
```

---

## 🚀 How to Upload to GitHub and Publish via GitHub Pages

### Step 1: Create a GitHub Repository
1. Log in to [GitHub](https://github.com/).
2. Click **New Repository**.
3. Name your repository (e.g., `corevo-interior`).
4. Set visibility to **Public**.
5. Click **Create repository**.

### Step 2: Upload Files to GitHub
Open your terminal in the project root folder and run:
```bash
# Initialize git
git init

# Stage all project files
git add .

# Create initial commit
git commit -m "Initial release of Corevo Interior landing page"

# Set main branch
git branch -M main

# Link to your GitHub repository (replace with your actual repository URL)
git remote add origin https://github.com/your-username/corevo-interior.git

# Push code to GitHub
git push -u origin main
```
*Alternatively, click "uploading an existing file" on GitHub's website interface and drag all files into the browser window.*

### Step 3: Publish via GitHub Pages
1. Go to your repository on GitHub.
2. Click **Settings** → **Pages** (in the left sidebar under Code and automation).
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **`main`** and folder **`/ (root)`**
4. Click **Save**.

Your live website URL will be published at:
`https://your-username.github.io/corevo-interior/`

---

## 🖼️ Local vs Cloud Placeholder Images

All images are saved locally in `assets/images/` with web-safe, lowercase, hyphens-only names:

| Image File Name | Description / Usage Section | Local Path |
| :--- | :--- | :--- |
| `hero-banner.png` | Hero section main background showcase | `assets/images/hero-banner.png` |
| `solution-design.png` | Approach card 1 (Practical & Beautiful) | `assets/images/solution-design.png` |
| `solution-budget.png` | Approach card 2 (Smart Budgeting) | `assets/images/solution-budget.png` |
| `solution-project.png` | Approach card 3 (End-to-End Handling) | `assets/images/solution-project.png` |
| `portfolio-living-room.png` | Portfolio Card 1 (Small condo makeover) | `assets/images/portfolio-living-room.png` |
| `portfolio-kitchen.png` | Portfolio Card 2 (Kitchen cabinet upgrade) | `assets/images/portfolio-kitchen.png` |
| `portfolio-bedroom.png` | Portfolio Card 3 (Muji-style bedroom design) | `assets/images/portfolio-bedroom.png` |
| `portfolio-dining.jpeg` | Portfolio Card 4 (Airbnb unit setup) | `assets/images/portfolio-dining.jpeg` |

---

## 📝 How to Edit Content, Images, CSS & JS

### 1. How to Replace Images
1. Save your new image into `assets/images/`.
2. Name the file with lowercase letters, numbers, and hyphens (e.g., `my-kitchen-renovation.jpg`). Avoid spaces, symbols, and non-ASCII characters.
3. Open `index.html` and update the `src` attribute:
   ```html
   <img src="assets/images/my-kitchen-renovation.jpg" alt="Kitchen renovation project" class="w-full h-44 object-cover">
   ```

### 2. How to Edit Text Content
Open `index.html` in any text editor:
- **Title**: Search `<title>` around line 10.
- **Headlines & Paragraphs**: Locate any section (`#hero`, `#services`, `#portfolio`, `#faq`, `#contact`) and edit text directly.

### 3. How to Update CSS
- Main production styles reside in `assets/css/style.css`.
- Source SASS file is in `assets/scss/style.scss`.
- Relative links are used throughout (`assets/css/style.css`), ensuring full subpath compatibility on GitHub Pages.

### 4. How to Update JavaScript
- Navigation scroll, mobile drawer, FAQ accordions, and WhatsApp lead form handler reside in `assets/js/main.js`.
- To update your WhatsApp receiver phone number, open `assets/js/main.js` and change `whatsappNumber` around line 261:
  ```javascript
  const whatsappNumber = "60103925762"; // Replace with your Malaysian mobile number (no plus or hyphens)
  ```

---

## 🔍 Troubleshooting Broken Images & Links on GitHub Pages

1. **Root Slash `/` Error**:
   - ❌ **Wrong**: `<img src="/assets/images/hero.png">` or `<link rel="stylesheet" href="/assets/css/style.css">`
   - ✅ **Correct**: `<img src="assets/images/hero.png">` or `<link rel="stylesheet" href="assets/css/style.css">`
   *Root slashes break on GitHub Pages subpaths like `https://username.github.io/repo-name/`.*

2. **Case Sensitivity**:
   - GitHub Pages runs on Linux servers, which are strictly case-sensitive.
   - `Hero-Banner.PNG` is **NOT** equal to `hero-banner.png`. Ensure exact filename case matching.

3. **Spaces & Special Characters**:
   - Always use hyphens (`-`) instead of spaces or special characters in filenames (e.g. `portfolio-kitchen.png`).

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
