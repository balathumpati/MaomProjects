# MaomProjects

# MaOM Projects: Group 16

A team project archive website for **Group 16 (MaOM, "Mastery Over Mind")**, CSE-H, Amrita Vishwa Vidyapeetham, Coimbatore.

**Live site:** https://maom-group16.vercel.app

## About

This is a static, single-page site that showcases the projects and activities done by the team. Each project appears as a card. Clicking a card opens a popup with its image or video and a full description. The page also lists the team members with their roll numbers and roles.

## Features

- Project cards loaded from a JSON file, so no code changes are needed to add a project
- "All Projects" dropdown for quick navigation to any project
- Popup viewer with image and/or video support
- Team details section loaded from a JSON file
- Responsive layout for mobile and desktop
- Keyboard accessible (Enter/Space to open a card, Esc to close)
- Respects reduced-motion settings
- No frameworks or build step: plain HTML, CSS and JavaScript

## Project Structure

```
MaomProjects/
├── index.html              # The whole site (markup, styles, script)
├── README.md
└── assets/
    ├── amritalogo.png      # University logo
    ├── projects/
    │   └── projects.json   # Project data (+ images/videos)
    └── team/
        └── team.json       # Team member data
```

## Adding a Project

Add an entry to `assets/projects/projects.json` and put its image or video in `assets/projects/`.

```json
[
  {
    "title": "Project Title",
    "summary": "One or two lines shown on the card.",
    "description": "Full description shown in the popup.",
    "image": "assets/projects/project-1.jpg",
    "video": "assets/projects/project-1.mp4"
  }
]
```

- `title`, `summary` and `description` are text.
- `image` and `video` are both optional. A project can use either, both, or neither.

## Adding Team Members

Edit `assets/team/team.json`:

```json
[
  { "name": "Member Name", "rollNo": "CB.XX.XXXXXXXXX", "role": "Role" }
]
```

`rollNo` and `role` are optional.

## Running Locally

The site loads its data with `fetch()`, so opening `index.html` directly (`file://`) won't work. Use a local server instead:

```bash
# Python
python -m http.server 8000

# or Node
npx serve .
```

Then open http://localhost:8000.

## Deployment

The site is static and can be hosted anywhere. It is currently deployed on **Vercel**, and it also works on **GitHub Pages**. Just push to `main`.

## Tech Stack

- HTML5, CSS3, vanilla JavaScript
- Google Fonts (Fraunces, Inter)

## Team

**Group 16, MaOM, CSE-H**
Amrita Vishwa Vidyapeetham, Coimbatore

See the live site for the full team list.
