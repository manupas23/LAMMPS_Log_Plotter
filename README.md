# LAMMPS Log Plotter 📊

An interactive, client-side, zero-dependency thermodynamic log analyzer and plotting dashboard for molecular dynamics simulations run in **LAMMPS**.

Built entirely as a single-page application (SPA) using HTML5, modern vanilla CSS, Plotly.js, FontAwesome, Google Fonts, and IndexedDB.

🚀 **Try the Live App here:** [https://manupas23.github.io/LAMMPS_Log_Plotter/](https://manupas23.github.io/LAMMPS_Log_Plotter/)

---

## Key Features 🚀

- 📂 **Drag & Drop Loading:** Easily load files by dragging them onto the workspace. Handles large files smoothly via an optimized line-by-line parser.
- 💾 **Persistent Session Storage:** Uses IndexedDB to securely store the parsed simulation log locally in your browser. Refreshing or returning to the page restores your last loaded session instantly without re-uploading.
- ⚡ **Multi-Phase Run Detection:** Automatically scans, parses, and indexes independent `run` command blocks from the log file as separate simulation phases. You can view individual runs or inspect a combined timeline.
- 📉 **Dual Y-Axis Support:** Plot multiple variables simultaneously on separate left (Y1) and right (Y2) axes, allowing you to easily correlate properties with different units or magnitudes (e.g., Temp vs. Volume).
- 🔍 **Interactive Plotly Visualization:** Pan, zoom, autoscale, customize titles/labels, and hovering highlights precise values.
- 📋 **Tabular Data View:** Inspect parsed data rows in a clean preview table and export them to a consolidated CSV.
- 🌓 **Instant Dark/Light Themes:** A premium, responsive interface featuring dynamic layouts, glassmorphism, and smooth transitions, fully adapting to system or user preferences.
- 🔒 **100% Client-Side:** No server uploads, no APIs, and no telemetry. All file parsing and database indexing happen locally in your web browser. Your simulation data never leaves your computer.

---

## How to Use 🛠️

### 1. Launch the Application
- **Option A:** Open `index.html` directly in any web browser.
- **Option B:** Visit the deployed version online via GitHub Pages (see Deployment below).

### 2. Load Simulation Log
Drag and drop your `log.lammps` (or any `.log`, `.dat`, `.txt` file containing LAMMPS thermodynamic outputs) into the dashed welcome area, or click to select the file manually.

### 3. Analyze and Plot
- **Select variables:** Use the sidebar checklist to toggle variables on the Y-axis.
- **Configure dual scales:** Check the "Dual Y-Axis" toggle and click the Y1/Y2 badges next to variable names to shift lines to the right axis.
- **Customize Labels:** Modify titles and axis labels directly from the inline customizer settings to prepare figures for publication.
- **Inspect Data:** Switch to the **Vista de Datos** (Data View) tab to preview the raw parsed values or click **Exportar CSV** to save.

---

## Folder Structure 📁

```text
LAMMPS_Log_Plotter/
├── index.html         # Self-contained web application (HTML, CSS, JS)
├── README.md          # Documentation
├── LICENSE            # MIT License
├── .gitignore         # Git ignore file for local environments
└── .github/
    └── workflows/
        └── deploy.yml # GitHub Actions workflow for auto-deployment to Pages
```

---

## Deployment to GitHub Pages 🌐

Deploying this application online is extremely simple:

1. **Create a GitHub repository:** Name it `LAMMPS_Log_Plotter`.
2. **Push files:** Initialize git in the folder and push to your repository.
3. **Configure Pages:**
   - Go to your repository settings on GitHub: **Settings** -> **Pages**.
   - Under **Build and deployment** -> **Source**, select **GitHub Actions**.
   - The included workflow in `.github/workflows/deploy.yml` will trigger on every push to `main` (or `master`) and automatically deploy the app to your custom GitHub Pages URL: `https://<your-username>.github.io/LAMMPS_Log_Plotter/`.

---

## Development & Tech Stack 💻

- **UI/UX:** Native CSS variables, Flexbox/Grid, and responsive queries. Font superfamily: *Outfit* (headings/UI) & *JetBrains Mono* (data tables). Icons by *FontAwesome 6*.
- **Plotting Engine:** [Plotly.js](https://plotly.com/javascript/) (loaded via CDN).
- **Local Database:** [IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) for zero-latency file persistence.

---

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
