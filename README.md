# 🌌 Satish Upadhyay | Professional Executive Portfolio

> **Futuristic, High-Performance Executive Portfolio** crafted in React, Tailwind CSS, and Motion. Built for showcasing senior programmatic execution, agile methodologies (CSM®, CSPO®), enterprise-scale product architecture, and consulting services.

---

## 🚀 Two Seamless Ways to Deploy to GitHub Pages

We have pre-configured this repository to support **both** automated CI/CD and traditional manual deployment workflows out of the box.

### Option A: 💎 Fully Automated via GitHub Actions (Recommended)
This is the modern standard. Every time you push code to `main` or `master`, GitHub will build and host your site automatically!

1. Open your repository on **GitHub**.
2. Navigate to **Settings** > **Pages** (under the Code and automation section).
3. Under **Build and deployment** > **Source**, select **GitHub Actions** from the dropdown menu.
4. Push your changes to your `main` or `master` branch. The pre-configured `.github/workflows/deploy.yml` pipeline will trigger automatically, build your code, and host it!

---

### Option B: 🛠️ Manual CLI Deployment (gh-pages)
If you prefer building and deploying manually from your computer's terminal:

1. Install all dependencies:
   ```bash
   npm install
   ```
2. Verify / configure your target domain mapping inside `package.json`:
   ```json
   "homepage": "https://satishkrupadhyay.github.io"
   ```
3. Run the automated deployment script:
   ```bash
   npm run deploy
   ```
   *This command compiles the project assets and pushes the generated `dist/` production assets directly to a clean `gh-pages` branch on your remote origin.*

---

## ⚙️ Path Customization for GitHub Pages

Before triggering your build, make sure to configure the correct asset root directory inside `/vite.config.ts` depending on your repository name:

- **Case 1: Primary User Site** (`satishkrupadhyay.github.io`)
  *If your repository is exactly your GitHub username.github.io, the URL runs on the root domain (`https://satishkrupadhyay.github.io/`).*
  Set `base: '/'` in `/vite.config.ts`:
  ```typescript
  base: '/',
  ```

- **Case 2: Secondary Project Site** (e.g. `/portfolio/`)
  *If your repository has another name, the URL runs under a subfolder path.*
  Set `base: '/portfolio/'` matching the repository name in `/vite.config.ts`:
  ```typescript
  base: '/portfolio/',
  ```

---

## 🛠️ Local Development & Quickstart

To run, inspect, and modify the portfolio source code on your local computer:

1. **Clone the repository:**
   ```bash
   git clone <your-repo-link>
   cd <your-repo-dir>
   ```
2. **Install core dependencies:**
   ```bash
   npm install
   ```
3. **Run local dev server:**
   ```bash
   npm run dev
   ```
   *Your browser will load the live high-fidelity hot-reloading dashboard at `http://localhost:3000`.*

---

## 🗂️ Project Architecture & Data Model

- **`/src/data.ts`**: Holds the comprehensive database, containing all your professional chronology, impact highlights, metrics, accolades, and scholastic background. To modify your portfolio, **simply update the items in this file**—the entire User Interface is dynamically computed from this model.
- **`/src/components/ResumePDFView.tsx`**: Renders the complete executive document paper view, enabling clients to view, download raw JSON data, or print-to-save as a styled PDF natively.
- **`/src/components/Experience.tsx`**: Dynamic experience chronicle showing full history or isolating metrics spotlight key results organically.
