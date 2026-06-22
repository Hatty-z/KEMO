# Event-Driven Keyframe Memory — Project Page

A static academic project website prepared for GitHub Pages. The structure and interaction patterns follow the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template), with project-specific sections for motivation, method, six real-world tasks, quantitative results, ablations, and BibTeX.

## Preview locally

Python 3:

```bash
cd KEMO-site
python3 -m http.server 8000
```

Open `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a new public repository, for example `event-driven-keyframe-memory`.
2. Copy all files in this folder to the repository root.
3. Push to the `main` branch:

```bash
git init
git add .
git commit -m "Initial project page"
git branch -M main
git remote add origin git@github.com:<YOUR_USERNAME>/event-driven-keyframe-memory.git
git push -u origin main
```

4. In GitHub, open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Select `main` and `/ (root)`, then save.
7. The page will appear at:

```text
https://<YOUR_USERNAME>.github.io/event-driven-keyframe-memory/
```

## Required edits before a public release

Search `index.html` for `TODO` and update:

- author names and profile links;
- institution and conference status;
- paper/supplementary PDFs;
- public code repository link;
- BibTeX metadata;
- title/description/preview metadata if the final paper title changes.

## Assets

```text
static/
├── css/index.css
├── js/index.js
├── images/
│   ├── framework.png
│   ├── keyframe_detector.png
│   ├── memory_integration.png
│   ├── stage_ambiguity.png
│   ├── social_preview.png
│   └── tasks/*.png
├── videos/
│   ├── teaser.mp4
│   └── tasks/*.mp4
└── pdfs/
    ├── paper.pdf
    └── supplementary.pdf
```

The current task clips were extracted from the supplied supplementary video. Replace them with clean task-specific clips by keeping the same filenames.

## Recommended video encoding

```bash
ffmpeg -i input.mp4 \
  -vf "scale=-2:720,fps=24" \
  -an -c:v libx264 -crf 27 -preset medium \
  -pix_fmt yuv420p -movflags +faststart output.mp4
```

## Template attribution

The footer retains attribution to the Academic Project Page Template and the Nerfies project page. Keep this attribution unless the upstream license permits a different form.
