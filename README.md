<!DOCTYPE html>
<html lang="en" data-theme="parchment">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Planner Studio Pro · Deep Work & Weekly Architect</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;0,9..144,700;1,9..144,400;1,9..144,600&family=JetBrains+Mono:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet" />

  <style>
    /* ==========================================================================
       THEME SYSTEM & DESIGN TOKENS
       ========================================================================== */
    :root, :root[data-theme="parchment"] {
      --bg: #f6f3eb;
      --bg-surface: #ffffff;
      --bg-subtle: #f0ebe0;
      --bg-hover: #e8e2d4;
      --text: #262320;
      --text-muted: #746e65;
      --text-subtle: #a49e93;
      --border: #e2dcd0;
      --border-dark: #cdcaa8;
      --accent: #bd4e32;
      --accent-hover: #a54026;
      --accent-light: #faece7;
      --accent-glow: rgba(189, 78, 50, 0.22);
      --green: #2e7d32;
      --green-light: #eaf5eb;
      --blue: #2563eb;
      --blue-light: #eff6ff;
      --purple: #7c3aed;
      --purple-light: #f5f3ff;
      --amber: #d97706;
      --amber-light: #fef3c7;
      --rose: #e11d48;
      --rose-light: #ffe4e6;
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.04);
      --shadow-sm: 0 3px 8px rgba(0,0,0,0.06);
      --shadow-md: 0 10px 28px rgba(0,0,0,0.08);
      --shadow-lg: 0 20px 40px rgba(0,0,0,0.12);
      --card-radius: 16px;
      --btn-radius: 9999px;
    }

    :root[data-theme="midnight"] {
      --bg: #0f1013;
      --bg-surface: #181a1f;
      --bg-subtle: #21242b;
      --bg-hover: #2c3039;
      --text: #f0f2f5;
      --text-muted: #959ba6;
      --text-subtle: #626875;
      --border: #292d36;
      --border-dark: #3f4553;
      --accent: #e06c4c;
      --accent-hover: #f17d5e;
      --accent-light: #2d1e1a;
      --accent-glow: rgba(224, 108, 76, 0.3);
      --green: #4ade80;
      --green-light: #132b1a;
      --blue: #60a5fa;
      --blue-light: #172a45;
      --purple: #c084fc;
      --purple-light: #2c1a42;
      --amber: #fbbf24;
      --amber-light: #362911;
      --rose: #f43f5e;
      --rose-light: #38131d;
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.4);
      --shadow-sm: 0 3px 8px rgba(0,0,0,0.5);
      --shadow-md: 0 10px 28px rgba(0,0,0,0.65);
      --shadow-lg: 0 20px 40px rgba(0,0,0,0.85);
    }

    :root[data-theme="forest"] {
      --bg: #121915;
      --bg-surface: #1a241f;
      --bg-subtle: #23302a;
      --bg-hover: #2e3f37;
      --text: #e6ede8;
      --text-muted: #93a59a;
      --text-subtle: #5f7368;
      --border: #2b3b33;
      --border-dark: #41574c;
      --accent: #52b788;
      --accent-hover: #74c69d;
      --accent-light: #162c21;
      --accent-glow: rgba(82, 183, 136, 0.28);
      --green: #52b788;
      --green-light: #193829;
      --blue: #64b5f6;
      --blue-light: #142838;
      --purple: #ba68c8;
      --purple-light: #2e1833;
      --amber: #ffd166;
      --amber-light: #382d12;
      --rose: #fb7185;
      --rose-light: #2d161d;
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.4);
      --shadow-sm: 0 3px 8px rgba(0,0,0,0.5);
      --shadow-md: 0 10px 28px rgba(0,0,0,0.65);
      --shadow-lg: 0 20px 40px rgba(0,0,0,0.85);
    }

    :root[data-theme="terracotta"] {
      --bg: #f9ede7;
      --bg-surface: #ffffff;
      --bg-subtle: #f3ded5;
      --bg-hover: #eacbbe;
      --text: #36221c;
      --text-muted: #826359;
      --text-subtle: #b6988f;
      --border: #e6c8bc;
      --border-dark: #d2a796;
      --accent: #c85a32;
      --accent-hover: #ae4823;
      --accent-light: #fae4dc;
      --accent-glow: rgba(200, 90, 50, 0.25);
      --green: #3d8b5c;
      --green-light: #e2f2e8;
      --blue: #3b82f6;
      --blue-light: #eef4ff;
      --purple: #8b5cf6;
      --purple-light: #f4f0ff;
      --amber: #d97706;
      --amber-light: #fef3c7;
      --rose: #e11d48;
      --rose-light: #ffe4e6;
      --shadow-xs: 0 1px 3px rgba(54,34,28,0.05);
      --shadow-sm: 0 3px 8px rgba(54,34,28,0.08);
      --shadow-md: 0 10px 28px rgba(54,34,28,0.12);
      --shadow-lg: 0 20px 40px rgba(54,34,28,0.16);
    }

    :root[data-theme="tokyo"] {
      --bg: #16161e;
      --bg-surface: #1f2335;
      --bg-subtle: #292e42;
      --bg-hover: #3b4261;
      --text: #c0caf5;
      --text-muted: #7aa2f7;
      --text-subtle: #565f89;
      --border: #292e42;
      --border-dark: #414868;
      --accent: #f7768e;
      --accent-hover: #ff9eaf;
      --accent-light: #341e2a;
      --accent-glow: rgba(247, 118, 142, 0.35);
      --green: #9ece6a;
      --green-light: #1f2f24;
      --blue: #7aa2f7;
      --blue-light: #1a2542;
      --purple: #bb9af7;
      --purple-light: #291e42;
      --amber: #e0af68;
      --amber-light: #3b2c19;
      --rose: #f7768e;
      --rose-light: #341e2a;
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.5);
      --shadow-sm: 0 3px 8px rgba(0,0,0,0.6);
      --shadow-md: 0 10px 28px rgba(0,0,0,0.75);
      --shadow-lg: 0 20px 40px rgba(0,0,0,0.9);
    }

    :root[data-theme="nord"] {
      --bg: #2e3440;
      --bg-surface: #3b4252;
      --bg-subtle: #434c5e;
      --bg-hover: #4c566a;
      --text: #eceff4;
      --text-muted: #88c0d0;
      --text-subtle: #d8dee9;
      --border: #434c5e;
      --border-dark: #4c566a;
      --accent: #88c0d0;
      --accent-hover: #8fbcbb;
      --accent-light: #2b383e;
      --accent-glow: rgba(136, 192, 208, 0.3);
      --green: #a3be8c;
      --green-light: #2a382e;
      --blue: #81a1c1;
      --blue-light: #223246;
      --purple: #b48ead;
      --purple-light: #362939;
      --amber: #ebcb8b;
      --amber-light: #3f3621;
      --rose: #bf616a;
      --rose-light: #3c2024;
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.4);
      --shadow-sm: 0 3px 8px rgba(0,0,0,0.5);
      --shadow-md: 0 10px 28px rgba(0,0,0,0.65);
      --shadow-lg: 0 20px 40px rgba(0,0,0,0.85);
    }

    /* ==========================================================================
       GLOBAL BASE & TYPOGRAPHY
       ========================================================================== */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      background-color: var(--bg);
      color: var(--text);
      font-family: "Plus Jakarta Sans", system-ui, -apple-system, sans-serif;
      line-height: 1.5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      overflow-x: hidden;
      transition: background-color 0.35s cubic-bezier(0.16, 1, 0.3, 1), color 0.35s ease;
    }

    #confetti-canvas {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 10000;
    }

    button, input, select, textarea {
      font-family: inherit;
      color: inherit;
      outline: none;
      border: none;
    }

    .app-shell {
      max-width: 1440px;
      margin: 0 auto;
      width: 100%;
      padding: 0 1.5rem 6rem 1.5rem;
      display: flex;
      flex-direction: column;
      flex: 1;
    }

    /* ==========================================================================
       STICKY HEADER (1 ROW: LEFT, CENTER, RIGHT)
       ========================================================================== */
    .sticky-header {
      position: sticky;
      top: 0;
      background-color: var(--bg);
      z-index: 50;
      padding: 1rem 0 0.8rem 0;
      border-bottom: 1px solid var(--border);
      backdrop-filter: blur(16px);
      transition: all 0.3s ease;
    }

    .header-top-grid {
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      align-items: center;
      gap: 1rem;
      width: 100%;
    }

    .header-left {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      gap: 0.5rem;
    }

    .header-center {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .header-right {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      gap: 0.45rem;
      flex-wrap: wrap;
    }

    .view-switcher {
      display: flex;
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.25rem;
      border-radius: var(--btn-radius);
      box-shadow: var(--shadow-xs);
      overflow-x: auto;
      max-width: 100%;
    }

    .view-btn {
      background: none;
      padding: 0.35rem 0.75rem;
      border-radius: var(--btn-radius);
      font-size: 0.78rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 0.3rem;
      white-space: nowrap;
      transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .view-btn:hover {
      color: var(--text);
    }
    .view-btn.active {
      background: var(--accent-light);
      color: var(--accent);
      box-shadow: 0 1px 3px var(--accent-glow);
    }

    .week-navigator {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.3rem 0.7rem 0.3rem 0.9rem;
      border-radius: var(--btn-radius);
      box-shadow: var(--shadow-xs);
    }

    .week-label-box {
      display: flex;
      flex-direction: column;
      align-items: center;
      min-width: 125px;
      user-select: none;
    }
    .week-label-box .date-range {
      font-size: 0.84rem;
      font-weight: 700;
      letter-spacing: -0.01em;
    }
    .week-label-box .rel-tag {
      font-size: 0.68rem;
      font-family: "JetBrains Mono", monospace;
      font-weight: 600;
      color: var(--accent);
    }

    .icon-nav-btn {
      background: none;
      color: var(--text-muted);
      cursor: pointer;
      font-size: 1.15rem;
      line-height: 1;
      padding: 0.25rem 0.5rem;
      border-radius: 6px;
      transition: all 0.15s cubic-bezier(0.2,0,0,1);
    }
    .icon-nav-btn:hover {
      background: var(--bg-hover);
      color: var(--text);
      transform: scale(1.15);
    }

    .btn-pill {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.42rem 0.85rem;
      border-radius: var(--btn-radius);
      font-size: 0.82rem;
      font-weight: 600;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      color: var(--text);
      box-shadow: var(--shadow-xs);
      transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .btn-pill:hover {
      background: var(--bg-hover);
      border-color: var(--border-dark);
      transform: translateY(-1px);
      box-shadow: var(--shadow-sm);
    }
    .btn-pill:active {
      transform: translateY(1px);
    }
    .btn-pill.primary {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
    }
    .btn-pill.primary:hover {
      background: var(--accent-hover);
      color: #ffffff;
    }

    .progress-strip {
      margin-top: 0.85rem;
      display: flex;
      align-items: center;
      gap: 1rem;
    }

    .progress-track {
      flex: 1;
      height: 9px;
      background: var(--bg-subtle);
      border-radius: 9999px;
      overflow: hidden;
      border: 1px solid var(--border);
      position: relative;
    }

    .progress-fill {
      height: 100%;
      width: 0%;
      border-radius: 9999px;
      background: linear-gradient(90deg, var(--accent), #f59e0b);
      box-shadow: 0 0 12px var(--accent-glow);
      transition: width 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .progress-metric {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.82rem;
      font-weight: 600;
      color: var(--text-muted);
      white-space: nowrap;
    }

    .filter-bar {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      margin-top: 1rem;
      flex-wrap: wrap;
    }

    .search-wrap {
      flex: 1;
      min-width: 220px;
      position: relative;
    }
    .search-input {
      width: 100%;
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.45rem 0.85rem 0.45rem 2.2rem;
      border-radius: var(--btn-radius);
      font-size: 0.84rem;
      box-shadow: var(--shadow-xs);
      transition: all 0.2s ease;
    }
    .search-input:focus {
      border-color: var(--accent);
      box-shadow: 0 0 0 3px var(--accent-glow);
      background: var(--bg-surface);
    }
    .search-icon {
      position: absolute;
      left: 0.75rem;
      top: 50%;
      transform: translateY(-50%);
      color: var(--text-subtle);
      pointer-events: none;
      font-size: 0.85rem;
    }

    .filter-pills {
      display: flex;
      gap: 0.35rem;
    }
    .filter-chip {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.3rem 0.7rem;
      border-radius: var(--btn-radius);
      font-size: 0.75rem;
      font-weight: 600;
      cursor: pointer;
      color: var(--text-muted);
      transition: all 0.15s ease;
    }
    .filter-chip:hover {
      background: var(--bg-hover);
      color: var(--text);
    }
    .filter-chip.active {
      background: var(--text);
      color: var(--bg);
      border-color: var(--text);
    }

    /* ==========================================================================
       VIEW PANELS & BOARD LAYOUT (FULL-WIDTH GRID MODE WITH FIXED LEFT BAR)
       ========================================================================== */
    .view-panel {
      display: none;
      animation: fadeInView 0.35s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .view-panel.active {
      display: block;
    }

    @keyframes fadeInView {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .board-layout {
      display: flex;
      gap: 2rem;
      margin-top: 1.5rem;
      align-items: flex-start;
      width: 100%;
    }

    .projects-column-section {
      width: 490px;
      min-width: 490px;
      flex-shrink: 0;
      transition: width 0.45s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .board-layout.tiles-only-mode .projects-column-section {
      width: 100%;
      min-width: 100%;
    }

    .timeline-column-section {
      flex: 1;
      min-width: 0;
      overflow: hidden;
      opacity: 1;
      transform: translateX(0);
      transition: opacity 0.35s ease, transform 0.35s ease, max-width 0.45s ease;
    }

    .board-layout.tiles-only-mode .timeline-column-section {
      opacity: 0;
      max-width: 0px;
      transform: translateX(30px);
      pointer-events: none;
      margin: 0;
      padding: 0;
    }

    .project-section-topbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 0.85rem;
      height: 34px;
      width: 490px;
      max-width: 490px;
    }

    .section-label-spaced {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.78rem;
      font-weight: 700;
      letter-spacing: 0.16em;
      color: var(--text-subtle);
      text-transform: uppercase;
    }

    .plan-actions-group {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      flex-wrap: wrap;
    }

    .btn-plan-action {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.32rem 0.65rem;
      border-radius: 8px;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.7rem;
      font-weight: 700;
      letter-spacing: 0.06em;
      cursor: pointer;
      color: var(--text-muted);
      transition: all 0.15s ease;
    }
    .btn-plan-action:hover {
      background: var(--bg-hover);
      color: var(--text);
      border-color: var(--border-dark);
      transform: translateY(-1px);
    }
    .btn-plan-action.active-toggle {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
    }

    /* ==========================================================================
       PROJECT CARDS & TASK ROWS
       ========================================================================== */
    #project-list-mount {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      width: 100%;
    }

    .board-layout.tiles-only-mode #project-list-mount {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 1.25rem;
    }

    .project-card {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      box-shadow: var(--shadow-sm);
      transition: box-shadow 0.25s ease, border-color 0.25s ease, transform 0.25s cubic-bezier(0.16, 1, 0.3, 1);
      position: relative;
      display: flex;
      flex-direction: column;
      overflow: hidden;
      animation: cardEntrance 0.35s cubic-bezier(0.16, 1, 0.3, 1) backwards;
    }
    .project-card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-2px);
    }

    @keyframes cardEntrance {
      from { opacity: 0; transform: translateY(14px) scale(0.98); }
      to { opacity: 1; transform: translateY(0) scale(1); }
    }

    .project-tile-banner {
      display: flex;
      align-items: center;
      padding: 1rem 1.25rem;
      gap: 0.85rem;
      border-bottom: 1px solid var(--border);
      background: var(--bg-surface);
      cursor: pointer;
    }

    .tile-badge-icon {
      width: 44px;
      height: 44px;
      border-radius: 8px;
      display: grid;
      place-items: center;
      font-size: 1.35rem;
      color: #ffffff;
      flex-shrink: 0;
      box-shadow: var(--shadow-xs);
      transition: transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .project-card:hover .tile-badge-icon {
      transform: scale(1.08) rotate(3deg);
    }

    .tile-badge-icon.theme-accent { background: var(--accent); }
    .tile-badge-icon.theme-blue { background: #1e3a8a; }
    .tile-badge-icon.theme-red { background: #881337; }
    .tile-badge-icon.theme-green { background: #14532d; }
    .tile-badge-icon.theme-purple { background: #4c1d95; }
    .tile-badge-icon.theme-amber { background: #b45309; }

    .project-card-body {
      padding: 1.15rem 1.25rem 0.9rem 1.25rem;
      display: flex;
      flex-direction: column;
      flex: 1;
    }

    .mini-project-progress-wrap {
      display: flex;
      align-items: center;
      gap: 0.55rem;
    }

    .mini-bar-track {
      width: 70px;
      height: 5px;
      background: var(--bg-subtle);
      border-radius: 9999px;
      overflow: hidden;
    }

    .mini-bar-fill {
      height: 100%;
      background: var(--accent);
      border-radius: 9999px;
      transition: width 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .project-ratio-label {
      font-family: "Fraunces", Georgia, serif;
      font-size: 0.88rem;
      color: var(--text-muted);
      font-weight: 500;
    }

    .task-card-list {
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      min-height: 40px;
    }

    .task-row-clean {
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
      padding: 0.45rem 0.4rem;
      border-radius: 8px;
      transition: background 0.15s ease, opacity 0.15s ease, transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
      position: relative;
    }
    .task-row-clean:hover {
      background: var(--bg-hover);
    }
    .task-row-clean.is-dragging {
      opacity: 0.35;
      transform: scale(0.97);
    }

    .task-main-line {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      width: 100%;
    }

    .task-drag-handle {
      cursor: grab;
      color: var(--text-subtle);
      font-size: 1.1rem;
      line-height: 1;
      padding: 0 0.15rem;
      opacity: 0.35;
      transition: opacity 0.15s ease, color 0.15s ease, transform 0.15s ease;
      user-select: none;
      display: grid;
      place-items: center;
    }
    .task-row-clean:hover .task-drag-handle {
      opacity: 0.9;
    }
    .task-drag-handle:active {
      cursor: grabbing;
      transform: scale(1.15);
    }

    .custom-check-box {
      appearance: none;
      width: 19px;
      height: 19px;
      border: 1.5px solid var(--border-dark);
      border-radius: 5px;
      background: var(--bg-surface);
      cursor: pointer;
      display: grid;
      place-content: center;
      flex-shrink: 0;
      transition: all 0.24s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .custom-check-box:checked {
      background: #3b6b4c;
      border-color: #3b6b4c;
      transform: scale(1.12);
    }
    .custom-check-box:checked::after {
      content: "✓";
      color: #ffffff;
      font-size: 11px;
      font-weight: 800;
      line-height: 1;
    }

    .task-title-serif {
      font-family: "Fraunces", Georgia, serif;
      font-size: 0.98rem;
      font-weight: 400;
      color: var(--text);
      flex: 1;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      cursor: pointer;
      transition: color 0.2s ease, text-decoration 0.2s ease;
    }

    .task-row-clean.completed-state .task-title-serif {
      text-decoration: line-through;
      color: var(--text-subtle);
    }

    .tag-pill-due {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: var(--btn-radius);
      padding: 0.18rem 0.6rem;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.72rem;
      color: var(--text-muted);
      white-space: nowrap;
      flex-shrink: 0;
    }

    .btn-assign-days-trigger {
      background: none;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.7rem;
      font-weight: 700;
      color: var(--accent);
      letter-spacing: 0.08em;
      cursor: pointer;
      padding: 0.2rem 0.4rem;
      border-radius: 4px;
      transition: all 0.15s ease;
      white-space: nowrap;
      text-transform: uppercase;
    }
    .btn-assign-days-trigger:hover {
      background: var(--accent-light);
    }

    .btn-task-open-details {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      width: 26px;
      height: 26px;
      border-radius: 6px;
      cursor: pointer;
      display: grid;
      place-items: center;
      color: var(--text-muted);
      font-size: 0.82rem;
      line-height: 1;
      opacity: 0.4;
      transition: all 0.18s cubic-bezier(0.34, 1.56, 0.64, 1);
      flex-shrink: 0;
    }
    .task-row-clean:hover .btn-task-open-details {
      opacity: 1;
    }
    .btn-task-open-details:hover {
      background: var(--accent-light);
      color: var(--accent);
      border-color: var(--accent);
      transform: scale(1.1);
    }

    .task-meta-subline {
      display: flex;
      align-items: center;
      gap: 0.45rem;
      padding-left: 3rem;
      margin-top: 0.05rem;
      flex-wrap: wrap;
    }

    .priority-badge {
      font-size: 0.62rem;
      font-weight: 700;
      text-transform: uppercase;
      padding: 0.08rem 0.35rem;
      border-radius: 4px;
      letter-spacing: 0.04em;
    }
    .priority-badge.high { background: var(--accent-light); color: var(--accent); }
    .priority-badge.med { background: var(--amber-light); color: var(--amber); }
    .priority-badge.low { background: var(--blue-light); color: var(--blue); }

    .subtasks-meter-chip {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.65rem;
      color: var(--text-muted);
      background: var(--bg-subtle);
      padding: 0.08rem 0.35rem;
      border-radius: 4px;
      font-weight: 600;
    }

    .btn-pin-zen {
      background: none;
      font-size: 0.72rem;
      cursor: pointer;
      opacity: 0.5;
      transition: opacity 0.15s ease, transform 0.15s ease;
    }
    .btn-pin-zen:hover {
      opacity: 1;
      transform: scale(1.2);
    }

    .day-selector-drawer {
      display: none;
      gap: 0.25rem;
      margin-top: 0.35rem;
      padding-left: 3rem;
      flex-wrap: wrap;
      animation: fadeInView 0.2s ease;
    }
    .day-selector-drawer.open {
      display: flex;
    }

    .day-toggle-chip {
      font-size: 0.68rem;
      font-weight: 700;
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: 4px;
      padding: 0.12rem 0.4rem;
      cursor: pointer;
      color: var(--text-muted);
      transition: all 0.15s ease;
    }
    .day-toggle-chip:hover {
      border-color: var(--accent);
      color: var(--accent);
    }
    .day-toggle-chip.active {
      background: var(--accent-light);
      border-color: var(--accent);
      color: var(--accent);
      font-weight: 800;
    }

    .task-subtasks-inline {
      padding-left: 3rem;
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      margin-top: 0.25rem;
    }
    .subtask-item-row {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      font-size: 0.78rem;
      color: var(--text-muted);
    }
    .subtask-item-row.is-done span {
      text-decoration: line-through;
      opacity: 0.6;
    }

    .project-card-footer-controls {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 0.85rem;
      padding-top: 0.75rem;
      border-top: 1px dashed var(--border);
      gap: 0.5rem;
    }

    .btn-project-add-task-trigger {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      background: none;
      color: var(--text-muted);
      font-size: 0.82rem;
      font-weight: 600;
      cursor: pointer;
      padding: 0.2rem 0.4rem;
      transition: all 0.15s ease;
    }
    .btn-project-add-task-trigger:hover {
      color: var(--accent);
      transform: translateX(2px);
    }

    .btn-toggle-expand-tasks {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      color: var(--text);
      font-family: "JetBrains Mono", monospace;
      font-size: 0.72rem;
      font-weight: 700;
      padding: 0.3rem 0.65rem;
      border-radius: 6px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      transition: all 0.18s ease;
      user-select: none;
    }
    .btn-toggle-expand-tasks:hover {
      background: var(--accent-light);
      color: var(--accent);
      border-color: var(--accent);
      transform: translateY(-1px);
    }
    .btn-toggle-expand-tasks.is-expanded {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
    }

    .icon-action-btn {
      background: none;
      color: var(--text-subtle);
      cursor: pointer;
      padding: 0.2rem 0.35rem;
      border-radius: 4px;
      font-size: 0.8rem;
      transition: all 0.15s ease;
    }
    .icon-action-btn:hover {
      background: var(--bg-hover);
      color: var(--text);
    }
    .icon-action-btn.danger:hover {
      color: #ef4444;
      background: rgba(239, 68, 68, 0.1);
    }

    /* ==========================================================================
       DAYS COLUMN SCHEDULE MATRIX & DRAGGABLE TASK CARDS
       ========================================================================== */
    .days-columns-grid {
      display: grid;
      grid-template-columns: repeat(7, minmax(130px, 1fr));
      gap: 0.75rem;
      overflow-x: auto;
      padding-bottom: 0.8rem;
    }

    .day-column {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 0.85rem;
      min-height: 440px;
      display: flex;
      flex-direction: column;
      box-shadow: var(--shadow-xs);
      transition: all 0.25s cubic-bezier(0.16, 1, 0.3, 1);
      position: relative;
    }
    .day-column.today-col {
      border-color: var(--accent);
      box-shadow: 0 0 0 2px var(--accent-glow);
      background: linear-gradient(180deg, var(--bg-surface) 0%, var(--bg-subtle) 100%);
    }
    .day-column.drag-over-active {
      border-color: var(--accent);
      background: var(--accent-light);
      transform: scale(1.02);
      box-shadow: var(--shadow-md);
    }

    .day-column-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border);
      padding-bottom: 0.6rem;
      margin-bottom: 0.75rem;
    }

    .day-name-tag {
      font-weight: 800;
      font-size: 0.88rem;
      letter-spacing: -0.01em;
    }
    .day-column.today-col .day-name-tag {
      color: var(--accent);
    }

    .day-num-badge {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--text-muted);
      background: var(--bg-subtle);
      padding: 0.1rem 0.4rem;
      border-radius: 4px;
    }

    .day-slot-bucket {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
    }

    .day-task-card {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 0.6rem 0.7rem;
      font-size: 0.82rem;
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      cursor: grab;
      transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
      user-select: none;
      position: relative;
    }
    .day-task-card:hover {
      transform: translateY(-2px);
      border-color: var(--border-dark);
      box-shadow: var(--shadow-sm);
    }
    .day-task-card:active {
      cursor: grabbing;
    }
    .day-task-card.is-done {
      opacity: 0.55;
      text-decoration: line-through;
    }

    .day-card-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 0.4rem;
    }

    .day-card-actions {
      display: flex;
      align-items: center;
      gap: 0.3rem;
    }

    .btn-tile-delete {
      background: none;
      border: none;
      font-size: 0.72rem;
      line-height: 1;
      color: var(--text-subtle);
      cursor: pointer;
      padding: 0.1rem 0.25rem;
      border-radius: 4px;
      opacity: 0.4;
      transition: all 0.15s ease;
    }
    .day-task-card:hover .btn-tile-delete {
      opacity: 0.9;
    }
    .btn-tile-delete:hover {
      color: #ef4444;
      background: rgba(239, 68, 68, 0.15);
      opacity: 1;
      transform: scale(1.15);
    }

    .project-pill-label {
      font-size: 0.65rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.03em;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      max-width: 90px;
    }

    /* ==========================================================================
       VIEW: EISENHOWER MATRIX (URGENT / IMPORTANT)
       ========================================================================== */
    .matrix-deck-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.25rem;
      margin-top: 1.5rem;
    }

    .matrix-quadrant {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.25rem;
      min-height: 280px;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      box-shadow: var(--shadow-sm);
      transition: all 0.25s ease;
    }
    .matrix-quadrant:hover {
      box-shadow: var(--shadow-md);
    }
    .matrix-quadrant.q1 { border-top: 4px solid var(--accent); }
    .matrix-quadrant.q2 { border-top: 4px solid var(--blue); }
    .matrix-quadrant.q3 { border-top: 4px solid var(--amber); }
    .matrix-quadrant.q4 { border-top: 4px solid var(--text-subtle); }

    .matrix-quad-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid var(--border);
      padding-bottom: 0.5rem;
    }

    .matrix-quad-title {
      font-family: "Fraunces", Georgia, serif;
      font-size: 1.15rem;
      font-weight: 700;
    }

    .matrix-quad-desc {
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    /* ==========================================================================
       VIEW: HABIT TRACKER & ROUTINES
       ========================================================================== */
    .habits-container {
      margin-top: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
    }

    .habit-card {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.1rem 1.4rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      box-shadow: var(--shadow-sm);
      transition: all 0.2s ease;
    }
    .habit-card:hover {
      transform: translateY(-2px);
      box-shadow: var(--shadow-md);
    }

    .habit-info-group {
      display: flex;
      align-items: center;
      gap: 0.85rem;
      flex: 1;
    }

    .habit-streak-flame {
      font-size: 1.2rem;
      font-weight: 800;
      color: var(--amber);
      display: flex;
      align-items: center;
      gap: 0.2rem;
      font-family: "JetBrains Mono", monospace;
    }

    .habit-days-row {
      display: flex;
      gap: 0.45rem;
    }

    .habit-check-pill {
      width: 32px;
      height: 32px;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: var(--bg-subtle);
      display: grid;
      place-items: center;
      font-size: 0.75rem;
      font-weight: 700;
      cursor: pointer;
      color: var(--text-muted);
      transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .habit-check-pill.checked {
      background: var(--green);
      color: #ffffff;
      border-color: var(--green);
      transform: scale(1.08);
    }

    /* ==========================================================================
       VIEW: HOURLY TIME-BLOCK PLANNER
       ========================================================================== */
    .timeblock-grid {
      display: grid;
      grid-template-columns: 80px repeat(7, 1fr);
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      overflow: hidden;
      margin-top: 1.5rem;
      box-shadow: var(--shadow-sm);
    }

    .tb-header-cell {
      padding: 0.75rem 0.5rem;
      text-align: center;
      font-weight: 700;
      font-size: 0.85rem;
      border-bottom: 2px solid var(--border);
      background: var(--bg-subtle);
    }

    .tb-time-label {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.72rem;
      color: var(--text-muted);
      padding: 0.6rem 0.5rem;
      text-align: right;
      border-bottom: 1px solid var(--border);
      border-right: 1px solid var(--border);
      background: var(--bg-subtle);
    }

    .tb-cell {
      border-bottom: 1px solid var(--border);
      border-right: 1px solid var(--border);
      min-height: 52px;
      padding: 0.25rem;
      transition: background 0.15s ease, box-shadow 0.15s ease;
      position: relative;
    }
    .tb-cell:hover {
      background: var(--bg-hover);
    }
    .tb-cell.drag-hover {
      background: var(--accent-light);
      box-shadow: inset 0 0 0 2px var(--accent);
    }

    .tb-event-badge {
      background: var(--accent);
      color: #ffffff;
      padding: 0.2rem 0.4rem;
      border-radius: 4px;
      font-size: 0.7rem;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      animation: fadeInView 0.2s ease;
    }

    /* ==========================================================================
       VIEW: GOOGLE CALENDAR
       ========================================================================== */
    .calendar-container {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.25rem 1.5rem;
      margin-top: 1.5rem;
      box-shadow: var(--shadow-sm);
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .cal-header-bar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .cal-title-date {
      font-family: "Fraunces", Georgia, serif;
      font-size: 1.6rem;
      font-weight: 700;
      color: var(--text);
    }

    .cal-grid-table {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      border-top: 1px solid var(--border);
      border-left: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
    }

    .cal-day-heading {
      background: var(--bg-subtle);
      border-right: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      padding: 0.75rem 0.5rem;
      text-align: center;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .cal-date-cell {
      min-height: 110px;
      border-right: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      padding: 0.45rem;
      background: var(--bg-surface);
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      transition: background 0.15s ease;
    }
    .cal-date-cell:hover {
      background: var(--bg-hover);
    }
    .cal-date-cell.other-month {
      background: var(--bg-subtle);
      opacity: 0.55;
    }
    .cal-date-cell.is-current-day {
      background: var(--accent-light);
    }

    .cal-date-cell-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.75rem;
      font-weight: 700;
      font-family: "JetBrains Mono", monospace;
      margin-bottom: 0.2rem;
    }
    .cal-date-cell.is-current-day .cal-date-num {
      background: var(--accent);
      color: #ffffff;
      border-radius: 50%;
      width: 22px;
      height: 22px;
      display: grid;
      place-items: center;
    }

    .cal-event-chip {
      background: var(--bg-subtle);
      border-left: 3px solid var(--accent);
      border-radius: 4px;
      padding: 0.2rem 0.35rem;
      font-size: 0.72rem;
      font-weight: 600;
      color: var(--text);
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 0.25rem;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      box-shadow: 0 1px 2px rgba(0,0,0,0.04);
      transition: all 0.15s ease;
    }
    .cal-event-chip:hover {
      transform: translateY(-1px);
    }
    .cal-event-chip.chip-done {
      opacity: 0.55;
      text-decoration: line-through;
      border-left-color: var(--green);
    }

    /* ==========================================================================
       VIEW: ANALYTICS & CHARTS
       ========================================================================== */
    .analytics-deck {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.25rem;
      margin-top: 1.5rem;
    }

    .stat-metric-card {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.4rem;
      display: flex;
      flex-direction: column;
      gap: 0.4rem;
      box-shadow: var(--shadow-xs);
    }

    .stat-metric-card .label {
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.04em;
    }

    .stat-metric-card .val {
      font-family: "Fraunces", Georgia, serif;
      font-size: 2.2rem;
      font-weight: 700;
      color: var(--text);
    }

    .heatmap-card {
      grid-column: 1 / -1;
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.4rem;
      box-shadow: var(--shadow-xs);
    }

    .heatmap-grid {
      display: grid;
      grid-template-flow: column;
      grid-template-rows: repeat(7, 14px);
      grid-auto-columns: 14px;
      gap: 3px;
      overflow-x: auto;
      padding: 1rem 0;
    }

    .heatmap-cell {
      width: 14px;
      height: 14px;
      border-radius: 2px;
      background: var(--bg-subtle);
      transition: transform 0.15s ease;
    }
    .heatmap-cell:hover {
      transform: scale(1.35);
      outline: 1px solid var(--text);
    }
    .heatmap-cell.l-1 { background: var(--green-light); border: 1px solid rgba(46, 125, 50, 0.2); }
    .heatmap-cell.l-2 { background: #81c784; }
    .heatmap-cell.l-3 { background: #4caf50; }
    .heatmap-cell.l-4 { background: var(--green); }

    .chart-box-grid {
      grid-column: 1 / -1;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.25rem;
    }

    .chart-card {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: var(--card-radius);
      padding: 1.25rem;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      box-shadow: var(--shadow-xs);
    }

    /* ==========================================================================
       ZEN FOCUS OVERLAY & BREATHING PACER
       ========================================================================== */
    .zen-overlay {
      position: fixed;
      inset: 0;
      background: var(--bg);
      z-index: 5000;
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem;
      animation: fadeInView 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .zen-overlay.active {
      display: flex;
    }

    .zen-breathing-orb {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      background: radial-gradient(circle, var(--accent-light) 0%, var(--accent-glow) 70%, transparent 100%);
      border: 2px solid var(--accent);
      display: grid;
      place-items: center;
      margin-bottom: 2rem;
      animation: breathPulse 8s ease-in-out infinite;
    }

    @keyframes breathPulse {
      0%, 100% { transform: scale(1); opacity: 0.7; }
      50% { transform: scale(1.4); opacity: 1; box-shadow: 0 0 35px var(--accent-glow); }
    }

    .zen-task-title {
      font-family: "Fraunces", Georgia, serif;
      font-size: 2.2rem;
      font-weight: 700;
      text-align: center;
      max-width: 680px;
      letter-spacing: -0.02em;
      margin-bottom: 0.5rem;
    }

    /* ==========================================================================
       SCRATCHPAD SLIDING DRAWER
       ========================================================================== */
    .scratchpad-drawer {
      position: fixed;
      top: 0;
      right: -360px;
      width: 340px;
      height: 100vh;
      background: var(--bg-surface);
      border-left: 1px solid var(--border-dark);
      box-shadow: var(--shadow-lg);
      z-index: 1500;
      padding: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      transition: right 0.35s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .scratchpad-drawer.open {
      right: 0;
    }

    .scratchpad-area {
      flex: 1;
      width: 100%;
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1rem;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.85rem;
      line-height: 1.6;
      color: var(--text);
      resize: none;
    }

    /* ==========================================================================
       FLOATING POMODORO HUD (WITH INLINE RESET & AUDIO/ALARM HUB)
       ========================================================================== */
    .floating-stack {
      position: fixed;
      bottom: 1.5rem;
      right: 1.5rem;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 0.75rem;
      z-index: 100;
    }

    .btn-assistant-trigger {
      background: var(--bg-surface);
      color: var(--text);
      border: 1px solid var(--border-dark);
      border-radius: 9999px;
      padding: 0.6rem 1.15rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.88rem;
      font-weight: 700;
      cursor: pointer;
      box-shadow: var(--shadow-md);
      backdrop-filter: blur(12px);
      transition: all 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .btn-assistant-trigger:hover {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
      transform: translateY(-2px) scale(1.04);
      box-shadow: 0 10px 24px var(--accent-glow);
    }

    .pomodoro-dock {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      border-radius: 9999px;
      padding: 0.45rem 0.9rem 0.45rem 0.55rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      box-shadow: var(--shadow-lg);
      backdrop-filter: blur(12px);
      position: relative;
    }

    .pomo-ring-wrap {
      width: 38px;
      height: 38px;
      position: relative;
      display: grid;
      place-items: center;
    }

    .pomo-info-col {
      display: flex;
      flex-direction: column;
      gap: 0.05rem;
    }

    .pomo-time-row {
      display: flex;
      align-items: center;
      gap: 0.35rem;
    }

    .pomo-time-readout {
      font-family: "JetBrains Mono", monospace;
      font-weight: 700;
      font-size: 0.95rem;
      letter-spacing: -0.02em;
    }

    .btn-pomo-adjust-time {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 6px;
      padding: 0.12rem 0.42rem;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.65rem;
      font-weight: 700;
      color: var(--text-muted);
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
      transition: all 0.15s ease;
      line-height: 1;
    }
    .btn-pomo-adjust-time:hover {
      background: var(--accent-light);
      color: var(--accent);
      border-color: var(--accent);
      transform: translateY(-1px);
    }

    .btn-pomo-reset-inline {
      background: none;
      font-size: 0.8rem;
      color: var(--text-subtle);
      cursor: pointer;
      padding: 0.1rem 0.25rem;
      border-radius: 4px;
      transition: all 0.18s ease;
      line-height: 1;
    }
    .btn-pomo-reset-inline:hover {
      color: var(--accent);
      transform: rotate(-90deg) scale(1.15);
    }

    .pomo-ctrl-btn {
      background: var(--accent);
      color: #ffffff;
      width: 32px;
      height: 32px;
      border-radius: 50%;
      cursor: pointer;
      display: grid;
      place-items: center;
      font-size: 0.85rem;
      transition: transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .pomo-ctrl-btn:hover {
      transform: scale(1.15);
    }

    .btn-ambient-sound {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      width: 32px;
      height: 32px;
      border-radius: 50%;
      cursor: pointer;
      display: grid;
      place-items: center;
      font-size: 0.85rem;
      color: var(--text-muted);
      transition: all 0.2s ease;
    }
    .btn-ambient-sound.active {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
      box-shadow: 0 0 8px var(--accent-glow);
    }

    .pomo-presets-popover {
      position: absolute;
      bottom: calc(100% + 10px);
      right: 0;
      background: var(--bg-surface);
      border: 1px solid var(--border-dark);
      border-radius: 12px;
      padding: 0.5rem;
      box-shadow: var(--shadow-lg);
      display: none;
      flex-direction: column;
      gap: 0.3rem;
      min-width: 140px;
      z-index: 105;
      animation: fadeInView 0.2s ease;
    }
    .pomo-presets-popover.open {
      display: flex;
    }

    .pomo-preset-btn {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      padding: 0.35rem 0.65rem;
      border-radius: 6px;
      font-size: 0.74rem;
      font-family: "JetBrains Mono", monospace;
      font-weight: 700;
      color: var(--text);
      cursor: pointer;
      text-align: left;
      display: flex;
      justify-content: space-between;
      transition: all 0.15s ease;
    }
    .pomo-preset-btn:hover {
      background: var(--accent-light);
      color: var(--accent);
      border-color: var(--accent);
    }
    .pomo-preset-btn.active {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
    }

    /* ==========================================================================
       MODALS & DIALOGS
       ========================================================================== */
    .modal-backdrop {
      position: fixed;
      inset: 0;
      background: rgba(40, 36, 30, 0.45);
      backdrop-filter: blur(8px);
      display: none;
      place-items: center;
      z-index: 2000;
      opacity: 0;
      transition: opacity 0.25s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .modal-backdrop.active {
      display: grid;
      opacity: 1;
    }

    .assistant-modal-card, .task-modal-card, .cmd-palette-box {
      background: var(--bg-surface);
      border: 1px solid var(--border-dark);
      border-radius: 20px;
      width: 92%;
      max-width: 540px;
      padding: 1.75rem 2rem 1.5rem;
      box-shadow: var(--shadow-lg);
      display: flex;
      flex-direction: column;
      gap: 1rem;
      animation: fadeInView 0.25s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .assistant-input-area, .modal-textarea {
      width: 100%;
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 0.85rem 1rem;
      font-size: 0.92rem;
      color: var(--text);
      resize: vertical;
      min-height: 80px;
    }

    .assistant-parsed-preview {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 0.85rem 1rem;
      font-size: 0.82rem;
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
    }
    .assistant-preview-row {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }
    .preview-key {
      font-family: "JetBrains Mono", monospace;
      font-weight: 700;
      color: var(--text-muted);
      font-size: 0.72rem;
      text-transform: uppercase;
      width: 75px;
    }
    .preview-val {
      font-weight: 600;
      color: var(--text);
    }

    .modal-project-tag {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.14em;
      color: var(--text-subtle);
      text-transform: uppercase;
    }

    .modal-task-title-input {
      font-family: "Fraunces", Georgia, serif;
      font-size: 1.55rem;
      font-weight: 600;
      color: var(--text);
      background: transparent;
      width: 100%;
      margin-top: -0.4rem;
      letter-spacing: -0.02em;
    }

    .modal-section-block {
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
    }

    .modal-section-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .modal-section-label {
      font-family: "JetBrains Mono", monospace;
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.12em;
      color: var(--text-subtle);
      text-transform: uppercase;
    }

    .btn-text-clear {
      background: none;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.7rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      color: var(--accent);
      cursor: pointer;
      text-transform: uppercase;
    }

    .modal-date-row {
      display: flex;
      gap: 0.75rem;
    }

    .modal-input-pill {
      background: var(--bg-subtle);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 0.6rem 0.85rem;
      font-family: "JetBrains Mono", monospace;
      font-size: 0.86rem;
      color: var(--text);
      display: flex;
      align-items: center;
      gap: 0.5rem;
      flex: 1;
    }
    .modal-input-pill input {
      background: transparent;
      width: 100%;
      font-size: inherit;
    }

    .modal-subtask-pills {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 0.35rem;
      margin-top: 0.2rem;
    }

    .btn-modal-day-pill {
      background: var(--bg-surface);
      border: 1px solid var(--border);
      padding: 0.4rem 0;
      border-radius: 8px;
      font-size: 0.75rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      text-align: center;
      transition: all 0.15s ease;
    }
    .btn-modal-day-pill.active {
      background: var(--accent);
      color: #ffffff;
      border-color: var(--accent);
      font-weight: 700;
    }

    .modal-subtask-list-builder {
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
      max-height: 120px;
      overflow-y: auto;
    }
    .modal-subtask-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      background: var(--bg-subtle);
      padding: 0.35rem 0.6rem;
      border-radius: 6px;
    }
    .modal-subtask-item input[type="text"] {
      background: transparent;
      flex: 1;
      font-size: 0.82rem;
    }

    .modal-footer-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 0.5rem;
      padding-top: 0.5rem;
    }

    .btn-modal-cancel {
      background: none;
      font-size: 0.86rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
    }

    .btn-modal-save {
      background: var(--text);
      color: var(--bg);
      font-size: 0.88rem;
      font-weight: 700;
      padding: 0.55rem 1.4rem;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.18s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .btn-modal-save:hover {
      background: var(--accent);
      color: #ffffff;
      transform: scale(1.03);
    }

    .cmd-search-header {
      display: flex;
      align-items: center;
      padding: 0.5rem 0.25rem 1rem;
      border-bottom: 1px solid var(--border);
      gap: 0.75rem;
    }
    .cmd-search-input {
      flex: 1;
      font-size: 1.05rem;
      background: transparent;
      color: var(--text);
    }

    .cmd-list {
      max-height: 300px;
      overflow-y: auto;
    }
    .cmd-item {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.65rem 0.85rem;
      border-radius: 8px;
      cursor: pointer;
      font-size: 0.88rem;
    }
    .cmd-item:hover {
      background: var(--accent-light);
      color: var(--accent);
    }

    /* TOAST NOTIFICATION CONTAINER */
    .toast-container {
      position: fixed;
      bottom: 1.5rem;
      left: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      z-index: 3000;
      pointer-events: none;
    }
    .toast-pill {
      background: var(--bg-surface);
      color: var(--text);
      border: 1px solid var(--border-dark);
      padding: 0.6rem 1rem;
      border-radius: 9999px;
      box-shadow: var(--shadow-md);
      font-size: 0.82rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      backdrop-filter: blur(12px);
      animation: slideInToast 0.3s cubic-bezier(0.34, 1.56, 0.64, 1) forwards;
      pointer-events: auto;
    }
    @keyframes slideInToast {
      from { opacity: 0; transform: translateY(16px) scale(0.9); }
      to { opacity: 1; transform: translateY(0) scale(1); }
    }

    @media (max-width: 1024px) {
      .header-top-grid {
        grid-template-columns: 1fr;
        gap: 0.75rem;
      }
      .header-left, .header-center, .header-right {
        justify-content: center;
      }
      .board-layout {
        flex-direction: column;
      }
      .projects-column-section {
        width: 100%;
        min-width: 100%;
      }
      .project-section-topbar {
        width: 100%;
        max-width: 100%;
      }
      .days-columns-grid {
        grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      }
      .matrix-deck-grid, .chart-box-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <canvas id="confetti-canvas"></canvas>
  <div class="toast-container" id="toast-container"></div>

  <!-- SCRATCHPAD DRAWER -->
  <aside class="scratchpad-drawer" id="scratchpad-drawer">
    <div style="display:flex; justify-content:space-between; align-items:center;">
      <h3 style="font-family:'Fraunces'; font-size:1.3rem;">Quick Scratchpad</h3>
      <button class="btn-text-clear" id="btn-close-scratchpad">CLOSE</button>
    </div>
    <div style="font-size:0.75rem; color:var(--text-muted);">Auto-saved brain dump & thoughts</div>
    <textarea class="scratchpad-area" id="scratchpad-input" placeholder="Draft notes, thoughts, and ideas here..."></textarea>
  </aside>

  <!-- ZEN FOCUS FULLSCREEN OVERLAY -->
  <div class="zen-overlay" id="zen-focus-overlay">
    <div class="zen-breathing-orb">
      <span style="font-family:'JetBrains Mono'; font-size:1.6rem; font-weight:700;" id="zen-pomo-readout">25:00</span>
    </div>
    <div class="zen-task-title" id="zen-active-task-title">Deep Work Focus Session</div>
    <div style="font-family:'JetBrains Mono'; font-size:0.85rem; color:var(--text-muted); margin-bottom: 2rem;">Breathe In (4s) · Hold (7s) · Exhale (8s)</div>
    <div style="display:flex; gap:1rem; align-items:center;">
      <button class="btn-pill primary" id="btn-zen-pomo-toggle">⏸ Pause</button>
      <button class="btn-pill" id="btn-exit-zen">✕ Exit Focus</button>
    </div>
  </div>

  <div class="app-shell">
    <!-- STICKY HEADER (1-ROW: LEFT, CENTER, RIGHT) -->
    <header class="sticky-header">
      <div class="header-top-grid">
        <!-- Left: View Switcher Tabs -->
        <div class="header-left">
          <nav class="view-switcher" aria-label="Views">
            <button class="view-btn active" data-view="board">
              <span>📋</span> Board
            </button>
            <button class="view-btn" data-view="matrix">
              <span>🎯</span> Matrix
            </button>
            <button class="view-btn" data-view="habits">
              <span>🌱</span> Habits
            </button>
            <button class="view-btn" data-view="calendar">
              <span>📅</span> Calendar
            </button>
            <button class="view-btn" data-view="timeblock">
              <span>⏰</span> Hourly
            </button>
            <button class="view-btn" data-view="analytics">
              <span>📊</span> Analytics
            </button>
          </nav>
        </div>

        <!-- Center: Week Navigator -->
        <div class="header-center">
          <div class="week-navigator">
            <button class="icon-nav-btn" id="btn-prev-week" title="Previous Week (Alt+←)">‹</button>
            <div class="week-label-box">
              <span class="date-range" id="week-date-display">...</span>
              <span class="rel-tag" id="week-rel-tag">This Week</span>
            </div>
            <button class="icon-nav-btn" id="btn-next-week" title="Next Week (Alt+→)">›</button>
          </div>
        </div>

        <!-- Right: Action Buttons Group -->
        <div class="header-right">
          <button class="btn-pill" id="btn-open-zen" title="Enter Zen Focus Mode">
            <span>🧘</span> Zen
          </button>
          <button class="btn-pill" id="btn-toggle-scratchpad" title="Open Scratchpad">
            <span>📝</span> Notes
          </button>
          <button class="btn-pill" id="btn-cmd-palette" title="Command Palette (Cmd/Ctrl + K)">
            <span style="font-family: 'JetBrains Mono'; font-size: 0.72rem; opacity: 0.7;">⌘K</span>
          </button>
          <button class="btn-pill" id="btn-theme-switcher" title="Toggle Themes">
            <span id="theme-emoji">🎨</span>
          </button>
          <button class="btn-pill" id="btn-shortcuts-help" title="Shortcuts (?)">
            <span>⌨️</span>
          </button>
          <button class="btn-pill primary" id="btn-quick-task">
            + Task
          </button>
        </div>
      </div>

      <div class="progress-strip">
        <div class="progress-track">
          <div class="progress-fill" id="master-progress-bar"></div>
        </div>
        <div class="progress-metric" id="master-progress-metric">0/0 · 0%</div>
      </div>

      <div class="filter-bar">
        <div class="search-wrap">
          <span class="search-icon">🔍</span>
          <input type="text" class="search-input" id="task-filter-input" placeholder="Filter tasks by name, #tag, or @project..." />
        </div>
        <div class="filter-pills">
          <button class="filter-chip active" data-filter="all">All</button>
          <button class="filter-chip" data-filter="high">High Priority</button>
          <button class="filter-chip" data-filter="pending">Pending</button>
          <button class="filter-chip" data-filter="completed">Done</button>
        </div>
      </div>
    </header>

    <!-- VIEW 1: WEEKLY BOARD -->
    <main class="view-panel active" id="view-board">
      <div class="board-layout" id="board-main-layout">
        <section class="projects-column-section">
          <div class="project-section-topbar">
            <span class="section-label-spaced">PROJECTS</span>
            <div class="plan-actions-group">
              <button class="btn-plan-action" id="btn-toggle-tiles" title="Toggle Grid / Split View">⊞ GRID</button>
              <button class="btn-plan-action" id="btn-open-backup-modal" title="Import / Export Data">DATA</button>
              <button class="btn-plan-action" id="btn-export-markdown" title="Export Plan to Markdown">MD</button>
              <button class="btn-plan-action" id="btn-copy-plan" title="Copy Plan to Clipboard">COPY</button>
              <button class="btn-plan-action" id="btn-paste-plan" title="Paste Plan from Clipboard">PASTE</button>
              <button class="btn-plan-action" id="btn-add-project-modal">+ NEW</button>
            </div>
          </div>
          <div id="project-list-mount"></div>
        </section>

        <section class="timeline-column-section" id="weekly-timeline-section">
          <div class="project-section-topbar" style="width: auto; max-width: none;">
            <span class="section-label-spaced">WEEKLY TIMELINE</span>
            <div style="font-size: 0.75rem; color: var(--text-muted); font-weight: 600;">Drag tasks between days to re-schedule</div>
          </div>
          <div class="days-columns-grid" id="days-columns-mount"></div>
        </section>
      </div>
    </main>

    <!-- VIEW 2: EISENHOWER MATRIX (URGENT / IMPORTANT) -->
    <section class="view-panel" id="view-matrix">
      <div class="project-section-topbar" style="margin-top: 1.5rem; width:100%; max-width:100%;">
        <span class="section-label-spaced">EISENHOWER DECISION MATRIX</span>
        <span style="font-size:0.8rem; color:var(--text-muted);">Urgency & Priority Alignment</span>
      </div>
      <div class="matrix-deck-grid" id="matrix-deck-mount"></div>
    </section>

    <!-- VIEW 3: HABITS & ROUTINE TRACKER -->
    <section class="view-panel" id="view-habits">
      <div class="project-section-topbar" style="margin-top: 1.5rem; width:100%; max-width:100%;">
        <span class="section-label-spaced">DAILY HABIT CADENCE</span>
        <button class="btn-plan-action" id="btn-add-habit-trigger">+ NEW HABIT</button>
      </div>
      <div class="habits-container" id="habits-list-mount"></div>
    </section>

    <!-- VIEW 4: GOOGLE CALENDAR VIEW -->
    <section class="view-panel" id="view-calendar">
      <div class="calendar-container">
        <div class="cal-header-bar">
          <div class="cal-title-date" id="cal-month-title">August 2026</div>
          <div class="cal-nav-group">
            <button class="btn-plan-action" id="btn-cal-today">Today</button>
            <button class="icon-nav-btn" id="btn-cal-prev">‹</button>
            <button class="icon-nav-btn" id="btn-cal-next">›</button>
          </div>
        </div>
        <div class="cal-grid-table" id="cal-grid-mount"></div>
      </div>
    </section>

    <!-- VIEW 5: HOURLY TIME-BLOCK PLANNER -->
    <section class="view-panel" id="view-timeblock">
      <div class="project-section-topbar" style="margin-top: 1.5rem; width:100%; max-width:100%;">
        <span class="section-label-spaced">HOURLY TIME-BLOCK MATRIX</span>
        <span style="font-size:0.8rem; color:var(--text-muted);">Drop tasks or click any slot to block focus time</span>
      </div>
      <div class="timeblock-grid" id="timeblock-grid-mount"></div>
    </section>

    <!-- VIEW 6: ANALYTICS & VELOCITY CHARTS -->
    <section class="view-panel" id="view-analytics">
      <div class="analytics-deck">
        <div class="stat-metric-card">
          <span class="label">Total Tasks Completed</span>
          <span class="val" id="stat-total-completed">0</span>
        </div>
        <div class="stat-metric-card">
          <span class="label">Focus Velocity Rate</span>
          <span class="val" id="stat-velocity-pct">0%</span>
        </div>
        <div class="stat-metric-card">
          <span class="label">Total Focus Minutes</span>
          <span class="val" id="stat-focus-time">0m</span>
        </div>
        
        <div class="chart-box-grid">
          <div class="chart-card">
            <span class="section-label-spaced">PRIORITY RATIO (SVG)</span>
            <div id="chart-priority-mount" style="height: 160px; display:flex; justify-content:center; align-items:center;"></div>
          </div>
          <div class="chart-card">
            <span class="section-label-spaced">DAY-OF-WEEK VOLUME</span>
            <div id="chart-day-mount" style="height: 160px; display:flex; justify-content:center; align-items:center;"></div>
          </div>
        </div>

        <div class="heatmap-card">
          <div class="project-section-topbar" style="width:100%; max-width:100%;">
            <span class="section-label-spaced">52-WEEK FOCUS CADENCE</span>
            <span style="font-size:0.75rem; color:var(--text-muted);">Daily completion intensity</span>
          </div>
          <div class="heatmap-grid" id="heatmap-grid-mount"></div>
        </div>
      </div>
    </section>
  </div>

  <!-- FLOATING ACTION HUD -->
  <div class="floating-stack">
    <button class="btn-assistant-trigger" id="btn-open-assistant" title="Prompt AI Assistant">
      <span>✨</span> Assistant
    </button>
    
    <aside class="pomodoro-dock" aria-label="Pomodoro Focus HUD">
      <!-- Session Presets Popover -->
      <div class="pomo-presets-popover" id="pomo-presets-popover">
        <div style="font-size: 0.65rem; font-weight:700; color:var(--text-muted); padding: 0.1rem 0.3rem;">FOCUS DURATION</div>
        <button class="pomo-preset-btn" onclick="setFocusSessionMinutes(15)"><span>15 min</span><span>⚡ Quick</span></button>
        <button class="pomo-preset-btn active" onclick="setFocusSessionMinutes(25)"><span>25 min</span><span>🎯 Standard</span></button>
        <button class="pomo-preset-btn" onclick="setFocusSessionMinutes(30)"><span>30 min</span><span>⏳ Medium</span></button>
        <button class="pomo-preset-btn" onclick="setFocusSessionMinutes(45)"><span>45 min</span><span>🧠 Deep</span></button>
        <button class="pomo-preset-btn" onclick="setFocusSessionMinutes(60)"><span>60 min</span><span>🔥 Power</span></button>
        <button class="pomo-preset-btn" onclick="setFocusSessionMinutes(90)"><span>90 min</span><span>🚀 Sprint</span></button>
      </div>

      <div class="pomo-ring-wrap">
        <svg width="38" height="38" viewBox="0 0 36 36">
          <path d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" fill="none" stroke="var(--border)" stroke-width="3"/>
          <path id="pomo-progress-arc" stroke-dasharray="100, 100" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" fill="none" stroke="var(--accent)" stroke-width="3" stroke-linecap="round"/>
        </svg>
      </div>

      <div class="pomo-info-col">
        <div class="pomo-time-row">
          <span class="pomo-time-readout" id="pomo-readout">25:00</span>
          <button class="btn-pomo-adjust-time" id="btn-open-pomo-presets" title="Change Duration">
            <span>⚙</span><span id="pomo-current-dur-tag">25m</span>
          </button>
          <button class="btn-pomo-reset-inline" id="btn-pomo-reset-trigger" title="Reset Session Timer">↺</button>
        </div>
        <div style="font-size: 0.65rem; color:var(--text-muted); font-weight:700;" id="pomo-state-label">FOCUS SESSION</div>
      </div>

      <!-- Button that triggers the Audio, Music & Alarm Hub Dialog Modal -->
      <button class="btn-ambient-sound" id="btn-open-audio-modal" title="Open Focus Audio & Alarm Hub">🎵</button>
      <button class="pomo-ctrl-btn" id="btn-pomo-toggle" title="Play/Pause">▶</button>
    </aside>
  </div>

  <!-- MODAL: PASTE A PLAN -->
  <div class="modal-backdrop" id="modal-paste-plan">
    <div class="task-modal-card" style="max-width: 480px; padding: 1.75rem 2rem;">
      <div style="display:flex; flex-direction:column; gap:0.35rem;">
        <span class="modal-project-tag" style="letter-spacing:0.18em; font-size:0.68rem; color:var(--text-subtle);">PASTE A PLAN</span>
        <h2 style="font-family:'Fraunces', Georgia, serif; font-size:1.55rem; font-weight:700; color:var(--text); margin-top:0.15rem;">Add a copied plan</h2>
        <p style="font-size:0.8rem; color:var(--text-muted); line-height:1.45; margin-top:0.25rem;">
          Paste a plan you copied from an archived week or another planner. It’s added below your current projects.
        </p>
      </div>

      <textarea 
        class="assistant-input-area" 
        id="paste-plan-input" 
        placeholder="Paste here with Cmd/Ctrl+V..." 
        style="min-height: 120px; font-family:'JetBrains Mono', monospace; font-size:0.8rem; line-height:1.4; margin-top:0.5rem;"></textarea>

      <label style="display:flex; align-items:center; gap:0.55rem; cursor:pointer; user-select:none; font-size:0.82rem; color:var(--text); margin-top:0.25rem;">
        <input type="checkbox" id="paste-reset-checkmarks" class="custom-check-box" checked style="width:17px; height:17px;" />
        <span>Reset checkmarks <span style="color:var(--text-muted); font-size:0.75rem;">(start fresh)</span></span>
      </label>

      <div class="modal-footer-row" style="margin-top:0.75rem;">
        <button class="btn-modal-cancel" id="btn-cancel-paste-modal">Cancel</button>
        <button class="btn-modal-save" id="btn-submit-paste-plan" style="background:#181a1f; color:#ffffff; padding:0.55rem 1.3rem; border-radius:8px;">Add to board</button>
      </div>
    </div>
  </div>

  <!-- MODAL: FOCUS AUDIO, MUSIC & ALARM HUB -->
  <div class="modal-backdrop" id="modal-audio-alarm-hub">
    <div class="task-modal-card">
      <div style="display:flex; justify-content:space-between; align-items:center;">
        <span class="modal-project-tag">FOCUS AUDIO & ALARM HUB</span>
        <button class="btn-text-clear" id="btn-close-audio-modal">CLOSE</button>
      </div>

      <h2 style="font-family:'Fraunces', Georgia, serif; font-size:1.5rem; letter-spacing:-0.02em;">Soundscapes & Timers</h2>

      <!-- Soundscape selector -->
      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">AMBIENT SOUNDSCAPE</span>
          <button class="btn-text-clear" onclick="setSoundscapeMode('off')">MUTE ALL</button>
        </div>
        <div class="modal-subtask-pills" style="grid-template-columns: repeat(4, 1fr);" id="audio-soundscape-buttons-mount">
          <button type="button" class="btn-modal-day-pill" onclick="setSoundscapeMode('rain')">🌧️ Rain</button>
          <button type="button" class="btn-modal-day-pill" onclick="setSoundscapeMode('binaural')">🧠 Gamma</button>
          <button type="button" class="btn-modal-day-pill" onclick="setSoundscapeMode('brown')">🌊 Ocean</button>
          <button type="button" class="btn-modal-day-pill" onclick="setSoundscapeMode('off')">🔇 Mute</button>
        </div>
      </div>

      <!-- Clock Alarm Selector -->
      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">SET ALARM AT SPECIFIC TIME</span>
          <button class="btn-text-clear" id="btn-clear-clock-alarm">CLEAR</button>
        </div>
        <div class="modal-date-row">
          <div class="modal-input-pill">
            <input type="time" id="alarm-time-input" />
          </div>
          <button class="btn-pill primary" id="btn-set-clock-alarm" style="border-radius:10px; padding:0.6rem 1.2rem;">Set Alarm</button>
        </div>
        <div id="alarm-status-tag" style="font-size:0.75rem; font-family:'JetBrains Mono'; color:var(--text-muted); margin-top:0.2rem;">No alarm scheduled</div>
      </div>

      <!-- Alarm Music / Tone Selector -->
      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">CHOOSE ALARM MUSIC / CHIME</span>
        </div>
        <div style="display:flex; gap:0.5rem;">
          <button type="button" class="btn-modal-day-pill active" id="btn-melody-bell" onclick="selectMelody('bell')" style="flex:1;">🔔 Celestial Bell</button>
          <button type="button" class="btn-modal-day-pill" id="btn-melody-harp" onclick="selectMelody('harp')" style="flex:1;">✨ Arpeggio Harp</button>
          <button type="button" class="btn-modal-day-pill" id="btn-melody-chime" onclick="selectMelody('chime')" style="flex:1;">🎶 Zen Chime</button>
        </div>
      </div>

      <div class="modal-footer-row">
        <button class="btn-modal-cancel" id="btn-cancel-audio-modal">Dismiss</button>
        <button class="btn-modal-save" id="btn-save-audio-modal">Done</button>
      </div>
    </div>
  </div>

  <!-- MODAL: AI ASSISTANT -->
  <div class="modal-backdrop" id="modal-ai-assistant">
    <div class="assistant-modal-card">
      <div style="display:flex; justify-content:space-between; align-items:center;">
        <span class="modal-project-tag">✨ PROMPT ARCHITECT ASSISTANT</span>
        <button class="btn-text-clear" id="btn-close-assistant">ESC</button>
      </div>
      
      <h3 style="font-family:'Fraunces', Georgia, serif; font-size:1.35rem; letter-spacing:-0.02em;">
        What would you like to schedule?
      </h3>

      <textarea class="assistant-input-area" id="assistant-prompt-input" placeholder="e.g. In project Deep Work & Strategy, create task Submit Final Report on Fri at 5:00 PM high priority"></textarea>

      <div class="assistant-parsed-preview" id="assistant-parsed-preview">
        <div class="assistant-preview-row"><span class="preview-key">Project:</span><span class="preview-val" id="preview-proj">-</span></div>
        <div class="assistant-preview-row"><span class="preview-key">Task:</span><span class="preview-val" id="preview-task">-</span></div>
        <div class="assistant-preview-row"><span class="preview-key">Schedule:</span><span class="preview-val" id="preview-schedule">-</span></div>
        <div class="assistant-preview-row"><span class="preview-key">Specs:</span><span class="preview-val" id="preview-specs">-</span></div>
      </div>

      <div class="modal-footer-row" style="margin-top:0.25rem;">
        <button class="btn-modal-cancel" id="btn-cancel-assistant">Cancel</button>
        <button class="btn-modal-save" id="btn-apply-assistant">✨ Generate & Add</button>
      </div>
    </div>
  </div>

  <!-- MODAL: TASK EDITOR PANEL WITH SUBTASKS -->
  <div class="modal-backdrop" id="modal-task-editor">
    <div class="task-modal-card">
      <div class="modal-project-tag" id="modal-task-proj-label">DEEP WORK & STRATEGY</div>
      <input type="text" class="modal-task-title-input" id="modal-task-title" placeholder="Task name..." />

      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">DEADLINE & TIME</span>
          <button class="btn-text-clear" id="btn-modal-clear-date">CLEAR</button>
        </div>
        <div class="modal-date-row">
          <div class="modal-input-pill">
            <input type="date" id="modal-deadline-date" />
          </div>
          <div class="modal-input-pill" style="max-width: 140px;">
            <input type="text" id="modal-deadline-time" placeholder="11:59 PM" value="11:59 PM" />
          </div>
        </div>
      </div>

      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">PRIORITY & ESTIMATE</span>
        </div>
        <div style="display:flex; gap:0.5rem;">
          <select id="modal-priority-select" class="modal-input-pill" style="padding:0.45rem 0.6rem; font-size:0.78rem;">
            <option value="high">High Priority</option>
            <option value="med" selected>Medium Priority</option>
            <option value="low">Low Priority</option>
          </select>
          <select id="modal-est-select" class="modal-input-pill" style="padding:0.45rem 0.6rem; font-size:0.78rem; max-width:140px;">
            <option value="15m">15m</option>
            <option value="30m">30m</option>
            <option value="45m" selected>45m</option>
            <option value="1h">1h</option>
            <option value="2h">2h</option>
          </select>
        </div>
      </div>

      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label" id="modal-subtasks-count-label">SCHEDULE DAYS</span>
        </div>
        <div class="modal-subtask-pills" id="modal-day-pills-mount"></div>
      </div>

      <!-- Checklist Builder -->
      <div class="modal-section-block">
        <div class="modal-section-header">
          <span class="modal-section-label">SUBTASKS & CHECKLIST</span>
          <button class="btn-text-clear" id="btn-add-modal-subtask">+ ADD ITEM</button>
        </div>
        <div class="modal-subtask-list-builder" id="modal-subtasks-builder-mount"></div>
      </div>

      <div class="modal-section-block">
        <span class="modal-section-label">DESCRIPTION (OPTIONAL)</span>
        <textarea class="modal-textarea" id="modal-description-input" placeholder="Overall note or context for this item..."></textarea>
      </div>

      <div class="modal-footer-row">
        <button class="btn-modal-cancel" id="btn-cancel-task-modal">Cancel</button>
        <button class="btn-modal-save" id="btn-save-task-modal">Save Task</button>
      </div>
    </div>
  </div>

  <!-- MODAL: DATA BACKUP & RESTORE -->
  <div class="modal-backdrop" id="modal-backup">
    <div class="cmd-palette-box">
      <div style="display:flex; justify-content:space-between; align-items:center;">
        <h3 style="font-family:'Fraunces'; font-size:1.3rem;">Data Backup & Export Suite</h3>
        <button class="btn-text-clear" onclick="document.getElementById('modal-backup').classList.remove('active')">ESC</button>
      </div>
      <div style="display:flex; flex-direction:column; gap:0.75rem; font-size:0.85rem;">
        <button class="btn-pill" id="btn-download-json-file">💾 Download Backup File (.json)</button>
        <button class="btn-pill" id="btn-export-csv-file">📊 Export Tasks to CSV</button>
        <div style="border-top:1px dashed var(--border); padding-top:0.75rem;">
          <span style="font-size:0.75rem; font-weight:700; color:var(--text-muted);">RESTORE FROM JSON FILE</span>
          <input type="file" id="backup-file-input" accept=".json" style="margin-top:0.5rem; font-size:0.8rem; width:100%;" />
        </div>
      </div>
    </div>
  </div>

  <!-- MODAL: COMMAND PALETTE -->
  <div class="modal-backdrop" id="modal-cmd-palette">
    <div class="cmd-palette-box">
      <div class="cmd-search-header">
        <span>⌘</span>
        <input type="text" class="cmd-search-input" id="cmd-input" placeholder="Type a command or search tasks..." />
        <span class="shortcut-badge" style="font-family:'JetBrains Mono'; font-size:0.7rem; color:var(--text-muted);">ESC</span>
      </div>
      <div class="cmd-list" id="cmd-results-mount"></div>
    </div>
  </div>

  <!-- MODAL: SHORTCUTS CHEAT SHEET -->
  <div class="modal-backdrop" id="modal-shortcuts">
    <div class="cmd-palette-box" style="max-width: 440px;">
      <div style="display:flex; justify-content:space-between; align-items:center;">
        <h3 style="font-family:'Fraunces'; font-size:1.3rem;">Keyboard Shortcuts</h3>
        <button class="btn-text-clear" onclick="document.getElementById('modal-shortcuts').classList.remove('active')">ESC</button>
      </div>
      <div style="display:flex; flex-direction:column; gap:0.6rem; font-size:0.85rem;">
        <div style="display:flex; justify-content:space-between;"><span>Command Palette</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">⌘ / Ctrl + K</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Quick Task</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">N</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Audio & Alarm Panel</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">A</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Zen Focus Mode</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">Z</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Toggle Notes</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">S</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Play/Pause Pomodoro</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">Space</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Switch Views (1-6)</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">1 · 2 · 3 · 4 · 5 · 6</kbd></div>
        <div style="display:flex; justify-content:space-between;"><span>Prev / Next Week</span><kbd style="font-family:'JetBrains Mono'; background:var(--bg-subtle); padding:2px 6px; border-radius:4px;">Alt + ← / →</kbd></div>
      </div>
    </div>
  </div>

  <!-- MODAL: CREATE PROJECT -->
  <div class="modal-backdrop" id="modal-new-project">
    <div class="cmd-palette-box" style="padding: 1.5rem;">
      <h3 style="font-family:'Fraunces'; font-size:1.3rem; margin-bottom:1rem;">New Focus Project</h3>
      <input type="text" class="modal-input-pill" id="new-project-name" placeholder="Project Name" style="width: 100%; margin-bottom: 1rem;" />
      <div style="display:flex; justify-content:flex-end; gap:0.5rem;">
        <button class="btn-pill" id="btn-cancel-proj">Cancel</button>
        <button class="btn-pill primary" id="btn-confirm-proj">Create</button>
      </div>
    </div>
  </div>

  <!-- ==========================================================================
       APPLICATION LOGIC & EVENT CONTROLLERS
       ========================================================================== -->
  <script>
    /* AUDIO SYNTHESIZER & SOUND ENGINE */
    class SoundEngine {
      constructor() {
        this.ctx = null;
        this.activeNoiseNode = null;
        this.activeNoiseGain = null;
        this.currentSoundMode = 'off';
        this.binauralOsc1 = null;
        this.binauralOsc2 = null;
        this.selectedMelody = 'bell';
      }
      init() {
        if (!this.ctx) {
          const AudioContext = window.AudioContext || window.webkitAudioContext;
          if (AudioContext) this.ctx = new AudioContext();
        }
      }
      playTick() {
        this.init();
        if (!this.ctx) return;
        const osc = this.ctx.createOscillator();
        const gain = this.ctx.createGain();
        osc.type = 'triangle';
        osc.frequency.setValueAtTime(440, this.ctx.currentTime);
        osc.frequency.exponentialRampToValueAtTime(880, this.ctx.currentTime + 0.05);
        gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, this.ctx.currentTime + 0.05);
        osc.connect(gain);
        gain.connect(this.ctx.destination);
        osc.start();
        osc.stop(this.ctx.currentTime + 0.05);
      }
      playComplete() {
        this.init();
        if (!this.ctx) return;
        const now = this.ctx.currentTime;
        [523.25, 659.25, 783.99, 1046.50].forEach((freq, i) => {
          const osc = this.ctx.createOscillator();
          const gain = this.ctx.createGain();
          osc.type = 'sine';
          osc.frequency.value = freq;
          gain.gain.setValueAtTime(0, now + i * 0.06);
          gain.gain.linearRampToValueAtTime(0.1, now + i * 0.06 + 0.02);
          gain.gain.exponentialRampToValueAtTime(0.001, now + i * 0.06 + 0.3);
          osc.connect(gain);
          gain.connect(this.ctx.destination);
          osc.start(now + i * 0.06);
          osc.stop(now + i * 0.06 + 0.35);
        });
      }
      playChime() {
        this.init();
        if (!this.ctx) return;
        const osc = this.ctx.createOscillator();
        const gain = this.ctx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(587.33, this.ctx.currentTime);
        osc.frequency.exponentialRampToValueAtTime(880, this.ctx.currentTime + 0.2);
        gain.gain.setValueAtTime(0.15, this.ctx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, this.ctx.currentTime + 0.4);
        osc.connect(gain);
        gain.connect(this.ctx.destination);
        osc.start();
        osc.stop(this.ctx.currentTime + 0.4);
      }
      playSelectedAlarm() {
        if (this.selectedMelody === 'harp') this.playComplete();
        else if (this.selectedMelody === 'chime') this.playChime();
        else this.playChime();
      }
      stopAmbient() {
        if (this.activeNoiseGain && this.ctx) {
          this.activeNoiseGain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + 0.4);
          setTimeout(() => {
            if (this.activeNoiseNode) this.activeNoiseNode.disconnect();
            if (this.binauralOsc1) { this.binauralOsc1.stop(); this.binauralOsc1.disconnect(); }
            if (this.binauralOsc2) { this.binauralOsc2.stop(); this.binauralOsc2.disconnect(); }
            this.currentSoundMode = 'off';
          }, 400);
        }
      }
      playRainNoise() {
        this.stopAmbient();
        this.init();
        const bufferSize = this.ctx.sampleRate * 2;
        const noiseBuffer = this.ctx.createBuffer(1, bufferSize, this.ctx.sampleRate);
        const output = noiseBuffer.getChannelData(0);
        let b0 = 0, b1 = 0, b2 = 0, b3 = 0, b4 = 0, b5 = 0, b6 = 0;
        for (let i = 0; i < bufferSize; i++) {
          const white = Math.random() * 2 - 1;
          b0 = 0.99886 * b0 + white * 0.0555179;
          b1 = 0.99332 * b1 + white * 0.0750759;
          b2 = 0.96900 * b2 + white * 0.1538520;
          b3 = 0.86650 * b3 + white * 0.3104856;
          b4 = 0.55000 * b4 + white * 0.5329522;
          b5 = -0.7616 * b5 - white * 0.0168980;
          output[i] = (b0 + b1 + b2 + b3 + b4 + b5 + b6 + white * 0.5362) * 0.04;
          b6 = white * 0.115926;
        }
        this.activeNoiseNode = this.ctx.createBufferSource();
        this.activeNoiseNode.buffer = noiseBuffer;
        this.activeNoiseNode.loop = true;

        this.activeNoiseGain = this.ctx.createGain();
        this.activeNoiseGain.gain.setValueAtTime(0.001, this.ctx.currentTime);
        this.activeNoiseGain.gain.exponentialRampToValueAtTime(0.18, this.ctx.currentTime + 0.6);

        this.activeNoiseNode.connect(this.activeNoiseGain);
        this.activeNoiseGain.connect(this.ctx.destination);
        this.activeNoiseNode.start();
        this.currentSoundMode = 'rain';
      }
      playBinauralFocus() {
        this.stopAmbient();
        this.init();
        this.binauralOsc1 = this.ctx.createOscillator();
        this.binauralOsc2 = this.ctx.createOscillator();
        this.binauralOsc1.frequency.setValueAtTime(200, this.ctx.currentTime);
        this.binauralOsc2.frequency.setValueAtTime(240, this.ctx.currentTime);

        this.activeNoiseGain = this.ctx.createGain();
        this.activeNoiseGain.gain.setValueAtTime(0.001, this.ctx.currentTime);
        this.activeNoiseGain.gain.exponentialRampToValueAtTime(0.08, this.ctx.currentTime + 0.6);

        this.binauralOsc1.connect(this.activeNoiseGain);
        this.binauralOsc2.connect(this.activeNoiseGain);
        this.activeNoiseGain.connect(this.ctx.destination);
        this.binauralOsc1.start();
        this.binauralOsc2.start();
        this.currentSoundMode = 'binaural';
      }
      playBrownNoise() {
        this.stopAmbient();
        this.init();
        const bufferSize = this.ctx.sampleRate * 2;
        const noiseBuffer = this.ctx.createBuffer(1, bufferSize, this.ctx.sampleRate);
        const output = noiseBuffer.getChannelData(0);
        let lastOut = 0.0;
        for (let i = 0; i < bufferSize; i++) {
          const white = Math.random() * 2 - 1;
          output[i] = (lastOut + (0.02 * white)) / 1.02;
          lastOut = output[i];
          output[i] *= 3.5;
        }
        this.activeNoiseNode = this.ctx.createBufferSource();
        this.activeNoiseNode.buffer = noiseBuffer;
        this.activeNoiseNode.loop = true;

        this.activeNoiseGain = this.ctx.createGain();
        this.activeNoiseGain.gain.setValueAtTime(0.001, this.ctx.currentTime);
        this.activeNoiseGain.gain.exponentialRampToValueAtTime(0.15, this.ctx.currentTime + 0.6);

        this.activeNoiseNode.connect(this.activeNoiseGain);
        this.activeNoiseGain.connect(this.ctx.destination);
        this.activeNoiseNode.start();
        this.currentSoundMode = 'brown';
      }
    }
    const sound = new SoundEngine();

    function setSoundscapeMode(mode) {
      if (mode === 'rain') sound.playRainNoise();
      else if (mode === 'binaural') sound.playBinauralFocus();
      else if (mode === 'brown') sound.playBrownNoise();
      else sound.stopAmbient();

      const btn = document.getElementById('btn-open-audio-modal');
      btn.classList.toggle('active', mode !== 'off');
      showToast(`Audio mode: ${mode.toUpperCase()}`, '🎵');
    }

    function selectMelody(melodyName) {
      sound.selectedMelody = melodyName;
      ['bell', 'harp', 'chime'].forEach(m => {
        const b = document.getElementById(`btn-melody-${m}`);
        if (b) b.classList.toggle('active', m === melodyName);
      });
      sound.playSelectedAlarm();
      showToast(`Alarm Melody: ${melodyName.toUpperCase()}`, '🔔');
    }

    /* AUDIO & ALARM MODAL HANDLERS */
    const audioAlarmModal = document.getElementById('modal-audio-alarm-hub');
    document.getElementById('btn-open-audio-modal').addEventListener('click', () => {
      audioAlarmModal.classList.add('active');
      sound.playTick();
    });
    document.getElementById('btn-close-audio-modal').addEventListener('click', () => audioAlarmModal.classList.remove('active'));
    document.getElementById('btn-cancel-audio-modal').addEventListener('click', () => audioAlarmModal.classList.remove('active'));
    document.getElementById('btn-save-audio-modal').addEventListener('click', () => audioAlarmModal.classList.remove('active'));

    /* ALARM CLOCK ENGINE */
    let activeAlarmTime = null;
    let alarmCheckInterval = null;

    document.getElementById('btn-set-clock-alarm').addEventListener('click', () => {
      const val = document.getElementById('alarm-time-input').value;
      if (!val) return;
      activeAlarmTime = val;
      document.getElementById('alarm-status-tag').textContent = `Active Alarm set for: ${val}`;
      sound.playTick();
      showToast(`Alarm set for ${val}`, '⏰');

      if (!alarmCheckInterval) {
        alarmCheckInterval = setInterval(() => {
          if (!activeAlarmTime) return;
          const now = new Date();
          const currentStr = `${now.getHours().toString().padStart(2, '0')}:${now.getMinutes().toString().padStart(2, '0')}`;
          if (currentStr === activeAlarmTime && now.getSeconds() === 0) {
            sound.playSelectedAlarm();
            launchCelebration();
            alert(`⏰ ALARM: It is now ${activeAlarmTime}!`);
            activeAlarmTime = null;
            document.getElementById('alarm-status-tag').textContent = 'No alarm scheduled';
          }
        }, 1000);
      }
    });

    document.getElementById('btn-clear-clock-alarm').addEventListener('click', () => {
      activeAlarmTime = null;
      document.getElementById('alarm-time-input').value = '';
      document.getElementById('alarm-status-tag').textContent = 'No alarm scheduled';
      sound.playTick();
      showToast('Alarm cleared', '🔕');
    });

    /* TOAST NOTIFICATION HELPER */
    function showToast(msg, icon = '✨') {
      const container = document.getElementById('toast-container');
      const toast = document.createElement('div');
      toast.className = 'toast-pill';
      toast.innerHTML = `<span>${icon}</span><span>${msg}</span>`;
      container.appendChild(toast);
      setTimeout(() => {
        toast.style.opacity = '0';
        toast.style.transform = 'translateY(10px)';
        toast.style.transition = 'all 0.3s ease';
        setTimeout(() => toast.remove(), 300);
      }, 3000);
    }

    /* STATE ARCHITECTURE & STORE */
    const DAYS_MAP = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'];
    const THEMES = ['parchment', 'midnight', 'forest', 'terracotta', 'tokyo', 'nord'];
    const TILE_THEMES = ['theme-accent', 'theme-blue', 'theme-red', 'theme-green', 'theme-purple', 'theme-amber'];
    const TILE_ICONS = ['🏛️', '✉️', '🛡️', '📊', '📚', '🎯', '💡', '🎓', '⚡', '🔬'];

    let appState = {
      weekOffset: 0,
      activeView: 'board',
      activeFilter: 'all',
      searchQuery: '',
      themeIndex: 0,
      isTilesView: false,
      expandedProjects: {},
      editingTaskId: null,
      editingProjectId: null,
      selectedModalDays: ['Mon'],
      modalSubtasks: [],
      calMonthOffset: 0,
      draggedTaskId: null,
      draggedFromProjId: null,
      draggedFromDay: null,
      zenPinnedTask: 'Deep Work Strategy Session',
      scratchpadContent: '',
      habits: [
        { id: 'h_1', title: 'Deep Work Block (90m)', streak: 12, days: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri'] },
        { id: 'h_2', title: 'Hydration & Mindful Break', streak: 8, days: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'] },
        { id: 'h_3', title: 'Architecture / Code Review', streak: 4, days: ['Mon', 'Wed', 'Fri'] }
      ],
      pomodoro: {
        focusDurationMinutes: 25,
        secondsLeft: 25 * 60,
        isRunning: false,
        timerId: null,
        mode: 'focus',
        totalFocusMinutes: 0
      },
      weeks: {}
    };

    function getWeekKey(offset) {
      const target = new Date();
      target.setDate(target.getDate() + offset * 7);
      const year = target.getFullYear();
      const firstDay = new Date(year, 0, 1);
      const pastDays = (target - firstDay) / 86400000;
      const weekNum = Math.ceil((pastDays + firstDay.getDay() + 1) / 7);
      return `${year}-W${weekNum}`;
    }

    function initCurrentWeekData() {
      const key = getWeekKey(appState.weekOffset);
      if (!appState.weeks[key]) {
        appState.weeks[key] = {
          projects: [
            {
              id: 'p_ml',
              name: 'Deep Work & Strategy',
              subtitle: 'Focus & Operations',
              tasks: [
                { id: 't_1', text: 'System Architecture Audit', completed: false, priority: 'high', isoDate: '', due: 'Aug 30 11:59 PM', est: '45m', days: ['Mon'], note: 'Review latency on microservices', subtasks: [{ id: 'st_1', text: 'Benchmark DB Queries', completed: true }, { id: 'st_2', text: 'Inspect Memory Pools', completed: false }] },
                { id: 't_2', text: 'Quarterly OKR Formulation', completed: false, priority: 'med', isoDate: '', due: 'No due date', est: '1h', days: ['Tue'], note: '', subtasks: [] },
                { id: 't_3', text: 'Client Review Preparation', completed: true, priority: 'low', isoDate: '', due: 'Sep 2 11:59 PM', est: '30m', days: ['Wed'], note: '', subtasks: [] }
              ]
            },
            {
              id: 'p_canvas',
              name: 'TAMUCT Online',
              subtitle: 'Canvas Learning Portal',
              tasks: [
                { id: 't_c1', text: 'Complete Modules 1-4', completed: false, priority: 'high', isoDate: '', due: 'Sep 5 11:59 PM', est: '2h', days: ['Tue'], note: '', subtasks: [] },
                { id: 't_c2', text: 'Discussion Board Synthesis', completed: true, priority: 'med', isoDate: '', due: 'Sep 6 11:59 PM', est: '30m', days: ['Wed'], note: '', subtasks: [] }
              ]
            }
          ]
        };
      }
      return appState.weeks[key];
    }

    function saveState() {
      localStorage.setItem('planner_studio_state', JSON.stringify({
        weeks: appState.weeks,
        themeIndex: appState.themeIndex,
        isTilesView: appState.isTilesView,
        expandedProjects: appState.expandedProjects,
        pomodoroDuration: appState.pomodoro.focusDurationMinutes,
        totalFocusMinutes: appState.pomodoro.totalFocusMinutes,
        scratchpadContent: appState.scratchpadContent,
        habits: appState.habits
      }));
      render();
    }

    function loadState() {
      const raw = localStorage.getItem('planner_studio_state');
      if (raw) {
        try {
          const parsed = JSON.parse(raw);
          if (parsed.weeks) appState.weeks = parsed.weeks;
          if (parsed.themeIndex !== undefined) appState.themeIndex = parsed.themeIndex;
          if (parsed.isTilesView !== undefined) appState.isTilesView = parsed.isTilesView;
          if (parsed.expandedProjects) appState.expandedProjects = parsed.expandedProjects;
          if (parsed.pomodoroDuration) {
            appState.pomodoro.focusDurationMinutes = parsed.pomodoroDuration;
            appState.pomodoro.secondsLeft = parsed.pomodoroDuration * 60;
          }
          if (parsed.totalFocusMinutes) appState.pomodoro.totalFocusMinutes = parsed.totalFocusMinutes;
          if (parsed.scratchpadContent) {
            appState.scratchpadContent = parsed.scratchpadContent;
            document.getElementById('scratchpad-input').value = parsed.scratchpadContent;
          }
          if (parsed.habits) appState.habits = parsed.habits;
        } catch (e) {
          console.error("State parse error", e);
        }
      }
      applyTheme(THEMES[appState.themeIndex] || 'parchment');
      initCurrentWeekData();
      updatePomoDisplay();
      render();
    }

    /* THEME MANAGER */
    function applyTheme(themeName) {
      document.documentElement.setAttribute('data-theme', themeName);
      const emojis = { parchment: '📜', midnight: '🌙', forest: '🌲', terracotta: '🏺', tokyo: '⚡', nord: '❄️' };
      document.getElementById('theme-emoji').textContent = emojis[themeName] || '🎨';
    }

    document.getElementById('btn-theme-switcher').addEventListener('click', () => {
      appState.themeIndex = (appState.themeIndex + 1) % THEMES.length;
      applyTheme(THEMES[appState.themeIndex]);
      sound.playTick();
      saveState();
      showToast(`Theme switched to ${THEMES[appState.themeIndex].toUpperCase()}`, '🎨');
    });

    /* CONFETTI CELEBRATION */
    function launchCelebration() {
      const canvas = document.getElementById('confetti-canvas');
      const ctx = canvas.getContext('2d');
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;

      const particles = Array.from({ length: 140 }, () => ({
        x: window.innerWidth / 2,
        y: window.innerHeight / 2,
        vx: (Math.random() - 0.5) * 18,
        vy: (Math.random() - 0.7) * 20,
        size: Math.random() * 7 + 4,
        color: ['#bd4e32', '#2e7d32', '#f59e0b', '#3b82f6', '#8b5cf6', '#ec4899'][Math.floor(Math.random() * 6)],
        rotation: Math.random() * 360,
        rSpeed: (Math.random() - 0.5) * 8,
        alpha: 1
      }));

      function frame() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        let active = false;
        particles.forEach(p => {
          p.x += p.vx;
          p.y += p.vy;
          p.vy += 0.45;
          p.rotation += p.rSpeed;
          p.alpha -= 0.012;
          if (p.alpha > 0) {
            active = true;
            ctx.save();
            ctx.globalAlpha = p.alpha;
            ctx.translate(p.x, p.y);
            ctx.rotate((p.rotation * Math.PI) / 180);
            ctx.fillStyle = p.color;
            ctx.fillRect(-p.size / 2, -p.size / 2, p.size, p.size);
            ctx.restore();
          }
        });
        if (active) requestAnimationFrame(frame);
        else ctx.clearRect(0, 0, canvas.width, canvas.height);
      }
      requestAnimationFrame(frame);
    }

    /* POMODORO CONTROLLERS (WITH INLINE RESET) */
    const pomoReadout = document.getElementById('pomo-readout');
    const zenPomoReadout = document.getElementById('zen-pomo-readout');
    const pomoStateLabel = document.getElementById('pomo-state-label');
    const pomoToggleBtn = document.getElementById('btn-pomo-toggle');
    const zenPomoToggleBtn = document.getElementById('btn-zen-pomo-toggle');
    const pomoArc = document.getElementById('pomo-progress-arc');
    const pomoPresetsPopover = document.getElementById('pomo-presets-popover');
    const btnOpenPomoPresets = document.getElementById('btn-open-pomo-presets');
    const pomoCurrentDurTag = document.getElementById('pomo-current-dur-tag');

    function updatePomoDisplay() {
      const m = Math.floor(appState.pomodoro.secondsLeft / 60);
      const s = appState.pomodoro.secondsLeft % 60;
      const formatted = `${m.toString().padStart(2, '0')}:${s.toString().padStart(2, '0')}`;
      pomoReadout.textContent = formatted;
      zenPomoReadout.textContent = formatted;
      const total = appState.pomodoro.mode === 'focus' ? appState.pomodoro.focusDurationMinutes * 60 : 5 * 60;
      const pct = (1 - appState.pomodoro.secondsLeft / total) * 100;
      pomoArc.style.strokeDasharray = `${pct}, 100`;
      pomoCurrentDurTag.textContent = `${appState.pomodoro.focusDurationMinutes}m`;
    }

    btnOpenPomoPresets.addEventListener('click', (e) => {
      e.stopPropagation();
      pomoPresetsPopover.classList.toggle('open');
      sound.playTick();
    });

    document.getElementById('btn-pomo-reset-trigger').addEventListener('click', (e) => {
      e.stopPropagation();
      clearInterval(appState.pomodoro.timerId);
      appState.pomodoro.isRunning = false;
      appState.pomodoro.secondsLeft = appState.pomodoro.focusDurationMinutes * 60;
      pomoToggleBtn.textContent = '▶';
      zenPomoToggleBtn.textContent = '▶ Resume';
      updatePomoDisplay();
      sound.playTick();
      showToast('Focus session reset', '↺');
    });

    document.addEventListener('click', (e) => {
      if (!pomoPresetsPopover.contains(e.target) && e.target !== btnOpenPomoPresets) {
        pomoPresetsPopover.classList.remove('open');
      }
    });

    window.setFocusSessionMinutes = function(mins) {
      appState.pomodoro.focusDurationMinutes = mins;
      if (appState.pomodoro.mode === 'focus') {
        appState.pomodoro.secondsLeft = mins * 60;
      }
      document.querySelectorAll('.pomo-preset-btn').forEach(btn => {
        btn.classList.toggle('active', btn.textContent.includes(`${mins} min`));
      });
      pomoPresetsPopover.classList.remove('open');
      sound.playTick();
      updatePomoDisplay();
      saveState();
    };

    function togglePomo() {
      sound.playTick();
      if (appState.pomodoro.isRunning) {
        clearInterval(appState.pomodoro.timerId);
        appState.pomodoro.isRunning = false;
        pomoToggleBtn.textContent = '▶';
        zenPomoToggleBtn.textContent = '▶ Resume';
      } else {
        appState.pomodoro.isRunning = true;
        pomoToggleBtn.textContent = '⏸';
        zenPomoToggleBtn.textContent = '⏸ Pause';
        appState.pomodoro.timerId = setInterval(() => {
          if (appState.pomodoro.secondsLeft > 0) {
            appState.pomodoro.secondsLeft--;
            if (appState.pomodoro.mode === 'focus' && appState.pomodoro.secondsLeft % 60 === 0) {
              appState.pomodoro.totalFocusMinutes++;
            }
            updatePomoDisplay();
          } else {
            sound.playSelectedAlarm();
            if (appState.pomodoro.mode === 'focus') {
              appState.pomodoro.mode = 'break';
              appState.pomodoro.secondsLeft = 5 * 60;
              pomoStateLabel.textContent = 'REST BREAK';
              launchCelebration();
            } else {
              appState.pomodoro.mode = 'focus';
              appState.pomodoro.secondsLeft = appState.pomodoro.focusDurationMinutes * 60;
              pomoStateLabel.textContent = 'FOCUS SESSION';
            }
            updatePomoDisplay();
          }
        }, 1000);
      }
    }
    pomoToggleBtn.addEventListener('click', togglePomo);
    zenPomoToggleBtn.addEventListener('click', togglePomo);

    /* ZEN OVERLAY HANDLERS */
    document.getElementById('btn-open-zen').addEventListener('click', () => {
      document.getElementById('zen-focus-overlay').classList.add('active');
      document.getElementById('zen-active-task-title').textContent = appState.zenPinnedTask;
      sound.playTick();
    });
    document.getElementById('btn-exit-zen').addEventListener('click', () => {
      document.getElementById('zen-focus-overlay').classList.remove('active');
    });

    window.pinTaskToZen = function(taskText) {
      appState.zenPinnedTask = taskText;
      showToast(`Task pinned to Zen Focus!`, '🧘');
      document.getElementById('btn-open-zen').click();
    };

    /* SCRATCHPAD DRAWER HANDLERS */
    const scratchpadDrawer = document.getElementById('scratchpad-drawer');
    const scratchpadInput = document.getElementById('scratchpad-input');
    document.getElementById('btn-toggle-scratchpad').addEventListener('click', () => {
      scratchpadDrawer.classList.toggle('open');
      sound.playTick();
      if (scratchpadDrawer.classList.contains('open')) scratchpadInput.focus();
    });
    document.getElementById('btn-close-scratchpad').addEventListener('click', () => {
      scratchpadDrawer.classList.remove('open');
    });
    scratchpadInput.addEventListener('input', (e) => {
      appState.scratchpadContent = e.target.value;
      saveState();
    });

    /* DATE COMPUTATION */
    function getWeekDates(offset) {
      const now = new Date();
      const currentDay = now.getDay();
      const diff = (currentDay === 0 ? -6 : 1) - currentDay;
      const monday = new Date(now);
      monday.setDate(now.getDate() + diff + offset * 7);

      return DAYS_MAP.map((_, i) => {
        const d = new Date(monday);
        d.setDate(monday.getDate() + i);
        return d;
      });
    }

    /* MARKDOWN DIGEST EXPORTER */
    document.getElementById('btn-export-markdown').addEventListener('click', () => {
      const week = initCurrentWeekData();
      const dates = getWeekDates(appState.weekOffset);
      let md = `# Weekly Plan Digest (${dates[0].toDateString()} – ${dates[6].toDateString()})\n\n`;
      week.projects.forEach(p => {
        md += `## 📁 ${p.name}\n`;
        p.tasks.forEach(t => {
          const status = t.completed ? '[x]' : '[ ]';
          const days = t.days.length ? ` (${t.days.join(', ')})` : '';
          md += `- ${status} **${t.text}** [${t.priority.toUpperCase()}]${days}\n`;
          if (t.subtasks && t.subtasks.length) {
            t.subtasks.forEach(st => {
              md += `  - ${st.completed ? '[x]' : '[ ]'} ${st.text}\n`;
            });
          }
        });
        md += `\n`;
      });
      navigator.clipboard.writeText(md).then(() => {
        sound.playComplete();
        showToast('Markdown Digest copied to clipboard!', '📋');
      });
    });

    /* DATA BACKUP & CSV EXPORTS */
    document.getElementById('btn-open-backup-modal').addEventListener('click', () => {
      document.getElementById('modal-backup').classList.add('active');
    });

    document.getElementById('btn-download-json-file').addEventListener('click', () => {
      const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(appState, null, 2));
      const dlAnchor = document.createElement('a');
      dlAnchor.setAttribute("href", dataStr);
      dlAnchor.setAttribute("download", `planner-backup-${new Date().toISOString().split('T')[0]}.json`);
      dlAnchor.click();
      sound.playComplete();
      showToast('Backup JSON downloaded!', '💾');
    });

    document.getElementById('btn-export-csv-file').addEventListener('click', () => {
      const week = initCurrentWeekData();
      let csv = 'Project,Task,Priority,Estimate,Scheduled Days,Completed\n';
      week.projects.forEach(p => {
        p.tasks.forEach(t => {
          csv += `"${p.name}","${t.text.replace(/"/g, '""')}","${t.priority}","${t.est}","${t.days.join(';')}","${t.completed}"\n`;
        });
      });
      const dataStr = "data:text/csv;charset=utf-8," + encodeURIComponent(csv);
      const dlAnchor = document.createElement('a');
      dlAnchor.setAttribute("href", dataStr);
      dlAnchor.setAttribute("download", `planner-tasks-${new Date().toISOString().split('T')[0]}.csv`);
      dlAnchor.click();
      sound.playComplete();
      showToast('Tasks exported to CSV!', '📊');
    });

    document.getElementById('backup-file-input').addEventListener('change', (e) => {
      const file = e.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = (event) => {
        try {
          const parsed = JSON.parse(event.target.result);
          if (parsed.weeks) {
            appState = Object.assign(appState, parsed);
            saveState();
            sound.playComplete();
            showToast('Backup restored successfully!', '✅');
            document.getElementById('modal-backup').classList.remove('active');
          }
        } catch (err) {
          alert('Invalid backup JSON file.');
        }
      };
      reader.readAsText(file);
    });

    /* COPY & PASTE PLAN FEATURE */
    document.getElementById('btn-copy-plan').addEventListener('click', () => {
      const week = initCurrentWeekData();
      navigator.clipboard.writeText(JSON.stringify(week.projects, null, 2)).then(() => {
        sound.playComplete();
        showToast('JSON Plan copied to clipboard!', '💾');
      });
    });

    /* PASTE A PLAN MODAL & PARSER (planner.plan.v1 support) */
    const pastePlanModal = document.getElementById('modal-paste-plan');
    const pastePlanInput = document.getElementById('paste-plan-input');
    const pasteResetCheckmarks = document.getElementById('paste-reset-checkmarks');

    document.getElementById('btn-paste-plan').addEventListener('click', () => {
      pastePlanInput.value = '';
      pastePlanModal.classList.add('active');
      sound.playTick();
      setTimeout(() => {
        pastePlanInput.focus();
        if (navigator.clipboard && navigator.clipboard.readText) {
          navigator.clipboard.readText().then(text => {
            if (text && (text.trim().startsWith('{') || text.trim().startsWith('['))) {
              pastePlanInput.value = text;
            }
          }).catch(() => {});
        }
      }, 100);
    });

    document.getElementById('btn-cancel-paste-modal').addEventListener('click', () => {
      pastePlanModal.classList.remove('active');
    });

    function formatDeadlineString(isoStr) {
      if (!isoStr) return 'No due date';
      try {
        const d = new Date(isoStr);
        if (isNaN(d.getTime())) return isoStr;
        const m = d.toLocaleDateString(undefined, { month: 'short', day: 'numeric' });
        let hours = d.getHours();
        const minutes = d.getMinutes().toString().padStart(2, '0');
        const ampm = hours >= 12 ? 'PM' : 'AM';
        hours = hours % 12 || 12;
        return `${m} ${hours}:${minutes} ${ampm}`;
      } catch (e) {
        return isoStr;
      }
    }

    document.getElementById('btn-submit-paste-plan').addEventListener('click', () => {
      const rawText = pastePlanInput.value.trim();
      if (!rawText) return;

      const resetDone = pasteResetCheckmarks.checked;
      const currentWeek = initCurrentWeekData();

      try {
        const parsed = JSON.parse(rawText);

        // Format A: planner.plan.v1 specification
        if (parsed.marker === 'planner.plan.v1' || (parsed.tasks && Array.isArray(parsed.tasks) && parsed.tasks.some(t => t.subs))) {
          (parsed.tasks || []).forEach((projItem, pIdx) => {
            const projectName = projItem.title || projItem.name || `Imported Project ${pIdx + 1}`;
            const newProject = {
              id: 'p_' + (projItem.id || Date.now() + '_' + pIdx),
              name: projectName,
              subtitle: 'Imported Plan',
              tasks: []
            };

            const subList = Array.isArray(projItem.subs) ? projItem.subs : (projItem.tasks || []);
            
            subList.forEach((sub, sIdx) => {
              const isoDate = sub.deadline ? sub.deadline.split('T')[0] : '';
              const daysAssigned = Array.isArray(sub.slots) && sub.slots.length > 0 
                ? sub.slots.map(s => s.day || s) 
                : [];

              newProject.tasks.push({
                id: 't_' + (sub.id || Date.now() + '_' + sIdx),
                text: sub.title || sub.text || 'Untitled Task',
                completed: resetDone ? false : !!sub.done,
                priority: sub.priority || 'med',
                isoDate: isoDate,
                due: formatDeadlineString(sub.deadline || sub.due),
                est: sub.est || '45m',
                days: daysAssigned,
                note: sub.desc || sub.note || '',
                subtasks: []
              });
            });

            currentWeek.projects.push(newProject);
          });

          sound.playComplete();
          launchCelebration();
          saveState();
          pastePlanModal.classList.remove('active');
          showToast('Plan added to board successfully!', '📋');
          return;
        }

        // Format B: Direct Project Array (native export format)
        if (Array.isArray(parsed)) {
          parsed.forEach(proj => {
            if (resetDone && Array.isArray(proj.tasks)) {
              proj.tasks.forEach(t => {
                t.completed = false;
                if (t.subtasks) t.subtasks.forEach(st => st.completed = false);
              });
            }
            currentWeek.projects.push(proj);
          });

          sound.playComplete();
          saveState();
          pastePlanModal.classList.remove('active');
          showToast('Plan restored from clipboard!', '✅');
          return;
        }

        alert('Unrecognized plan JSON format.');
      } catch (err) {
        alert('Invalid JSON: Please ensure you copied the complete plan object.');
      }
    });

    /* AI NATURAL LANGUAGE PARSER */
    function parseAssistantPrompt(text) {
      let result = {
        projectName: '',
        taskText: '',
        priority: 'med',
        est: '45m',
        days: [],
        dueTime: '11:59 PM',
        isoDate: '',
        dueFormatted: ''
      };
      if (!text || !text.trim()) return result;
      if (/\b(high\s*priority|urgent|asap|crit|p1)\b/i.test(text)) result.priority = 'high';
      else if (/\b(low\s*priority|minor|trivial|p3)\b/i.test(text)) result.priority = 'low';
      else result.priority = 'med';

      const estMatch = text.match(/\b(\d+(?:\.\d+)?\s*(?:h|hr|hrs|hours?|m|min|mins|minutes?))\b/i);
      if (estMatch) {
        let val = estMatch[1].toLowerCase().replace(/\s+/g, '');
        if (val.includes('h')) result.est = val.replace(/hours?|hrs?/, 'h');
        else if (val.includes('m')) result.est = val.replace(/minutes?|mins?/, 'm');
      }

      const timeMatch = text.match(/\b(?:at|by)\s*(\d{1,2}(?::\d{2})?\s*(?:am|pm)?)\b/i);
      if (timeMatch) {
        let t = timeMatch[1].toUpperCase().trim();
        if (!t.includes('AM') && !t.includes('PM')) t += ' PM';
        result.dueTime = t;
      }

      const dayKeywords = {
        'monday|mon': 'Mon', 'tuesday|tue': 'Tue', 'wednesday|wed': 'Wed',
        'thursday|thu|thur': 'Thu', 'friday|fri': 'Fri', 'saturday|sat': 'Sat', 'sunday|sun': 'Sun'
      };
      for (const [pattern, code] of Object.entries(dayKeywords)) {
        const re = new RegExp(`\\b(${pattern})\\b`, 'i');
        if (re.test(text)) {
          if (!result.days.includes(code)) result.days.push(code);
        }
      }

      const projMatch = text.match(/(?:in|under|to|for|create)?\s*(?:project|backlog)\s*["']?([^,\n\.\-\;]+?)["']?(?:,|\.|\s+(?:create|add|with|task|called|inside))/i);
      if (projMatch) result.projectName = projMatch[1].trim();

      let taskMatch = text.match(/(?:task|item|todo)\s*(?:called|named|is)?\s*["']?([^,\n\.\;]+?)["']?(?=\s+(?:due|by|on|at|priority|with|est|for)|$|\.|\,)/i);
      if (!taskMatch) {
        taskMatch = text.match(/(?:create|add)\s+["']?([^,\n\.\;]+?)["']?(?=\s+(?:due|by|on|at|priority|with|est|in project|to project)|$|\.|\,)/i);
      }
      if (taskMatch) {
        let candidate = taskMatch[1].trim().replace(/^(?:a|an|the)\s+/i, '');
        if (candidate.toLowerCase().startsWith('task ')) candidate = candidate.slice(5).trim();
        result.taskText = candidate;
      } else {
        result.taskText = text.trim();
      }

      const now = new Date();
      result.isoDate = now.toISOString().split('T')[0];
      if (result.days.length > 0) result.dueFormatted = `${result.days[0]} ${result.dueTime}`;
      else result.dueFormatted = `Due ${result.dueTime}`;
      return result;
    }

    const assistantModal = document.getElementById('modal-ai-assistant');
    const assistantInput = document.getElementById('assistant-prompt-input');

    function openAssistantModal() {
      assistantModal.classList.add('active');
      assistantInput.value = '';
      updateAssistantPreview('');
      setTimeout(() => assistantInput.focus(), 100);
      sound.playTick();
    }
    function closeAssistantModal() { assistantModal.classList.remove('active'); }

    function updateAssistantPreview(text) {
      const parsed = parseAssistantPrompt(text);
      const week = initCurrentWeekData();
      const defaultProj = week.projects[0] ? week.projects[0].name : 'Default Project';
      document.getElementById('preview-proj').textContent = parsed.projectName || defaultProj;
      document.getElementById('preview-task').textContent = parsed.taskText || '(Enter prompt above)';
      document.getElementById('preview-schedule').textContent = parsed.days.length > 0 ? parsed.days.join(', ') : 'Unscheduled';
      document.getElementById('preview-specs').textContent = `Priority: ${parsed.priority.toUpperCase()} · Est: ${parsed.est} · Time: ${parsed.dueTime}`;
    }

    assistantInput.addEventListener('input', (e) => updateAssistantPreview(e.target.value));
    document.getElementById('btn-open-assistant').addEventListener('click', openAssistantModal);
    document.getElementById('btn-close-assistant').addEventListener('click', closeAssistantModal);
    document.getElementById('btn-cancel-assistant').addEventListener('click', closeAssistantModal);

    document.getElementById('btn-apply-assistant').addEventListener('click', () => {
      const prompt = assistantInput.value.trim();
      if (!prompt) return;
      const parsed = parseAssistantPrompt(prompt);
      const week = initCurrentWeekData();
      let targetProj = null;
      if (parsed.projectName) {
        targetProj = week.projects.find(p => p.name.toLowerCase() === parsed.projectName.toLowerCase());
        if (!targetProj) {
          targetProj = {
            id: 'p_' + Date.now(),
            name: parsed.projectName.charAt(0).toUpperCase() + parsed.projectName.slice(1),
            tasks: []
          };
          week.projects.push(targetProj);
        }
      } else {
        targetProj = week.projects[0] || { id: 'p_' + Date.now(), name: 'Main Project', tasks: [] };
      }

      targetProj.tasks.push({
        id: 't_' + Date.now(),
        text: parsed.taskText || 'New Action Item',
        completed: false,
        priority: parsed.priority,
        isoDate: parsed.isoDate,
        due: parsed.dueFormatted,
        est: parsed.est,
        days: parsed.days.length > 0 ? parsed.days : ['Mon'],
        subtasks: [],
        note: `Generated via Assistant: "${prompt}"`
      });

      sound.playComplete();
      launchCelebration();
      saveState();
      closeAssistantModal();
      showToast('Task architected successfully!', '✨');
    });

    /* TASK MODAL & SUBTASKS ENGINE */
    const taskModalBackdrop = document.getElementById('modal-task-editor');

    window.openTaskModal = function(projectId, taskId = null) {
      appState.editingProjectId = projectId;
      appState.editingTaskId = taskId;

      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === projectId);
      document.getElementById('modal-task-proj-label').textContent = proj ? proj.name : 'PROJECT';

      if (taskId) {
        const task = proj ? proj.tasks.find(t => t.id === taskId) : null;
        if (task) {
          document.getElementById('modal-task-title').value = task.text;
          document.getElementById('modal-priority-select').value = task.priority || 'med';
          document.getElementById('modal-est-select').value = task.est || '45m';
          document.getElementById('modal-description-input').value = task.note || '';
          document.getElementById('modal-deadline-date').value = task.isoDate || '';
          appState.selectedModalDays = [...(task.days || [])];
          appState.modalSubtasks = (task.subtasks || []).map(st => ({ ...st }));
        }
      } else {
        document.getElementById('modal-task-title').value = '';
        document.getElementById('modal-priority-select').value = 'med';
        document.getElementById('modal-est-select').value = '45m';
        document.getElementById('modal-description-input').value = '';
        document.getElementById('modal-deadline-date').value = '';
        appState.selectedModalDays = ['Mon'];
        appState.modalSubtasks = [];
      }

      renderModalDayPills();
      renderModalSubtasks();
      taskModalBackdrop.classList.add('active');
      setTimeout(() => document.getElementById('modal-task-title').focus(), 100);
      sound.playTick();
    };

    function closeTaskModal() {
      taskModalBackdrop.classList.remove('active');
      appState.editingTaskId = null;
      appState.editingProjectId = null;
    }

    function renderModalDayPills() {
      const mount = document.getElementById('modal-day-pills-mount');
      mount.innerHTML = DAYS_MAP.map(day => {
        const isActive = appState.selectedModalDays.includes(day);
        return `<button type="button" class="btn-modal-day-pill ${isActive ? 'active' : ''}" onclick="toggleModalDay('${day}')">${day}</button>`;
      }).join('');
    }

    window.toggleModalDay = function(day) {
      if (appState.selectedModalDays.includes(day)) {
        appState.selectedModalDays = appState.selectedModalDays.filter(d => d !== day);
      } else {
        appState.selectedModalDays.push(day);
      }
      renderModalDayPills();
      sound.playTick();
    };

    function renderModalSubtasks() {
      const mount = document.getElementById('modal-subtasks-builder-mount');
      mount.innerHTML = appState.modalSubtasks.map((st, i) => `
        <div class="modal-subtask-item">
          <input type="checkbox" ${st.completed ? 'checked' : ''} onchange="appState.modalSubtasks[${i}].completed = this.checked">
          <input type="text" value="${st.text}" oninput="appState.modalSubtasks[${i}].text = this.value" placeholder="Subtask details...">
          <button class="icon-action-btn danger" onclick="appState.modalSubtasks.splice(${i}, 1); renderModalSubtasks();">✕</button>
        </div>
      `).join('') || '<span style="font-size:0.75rem; color:var(--text-subtle);">No subtasks added yet</span>';
    }

    document.getElementById('btn-add-modal-subtask').addEventListener('click', () => {
      appState.modalSubtasks.push({ id: 'st_' + Date.now(), text: '', completed: false });
      renderModalSubtasks();
      sound.playTick();
    });

    document.getElementById('btn-modal-clear-date').addEventListener('click', () => {
      document.getElementById('modal-deadline-date').value = '';
      sound.playTick();
    });

    document.getElementById('btn-cancel-task-modal').addEventListener('click', closeTaskModal);

    document.getElementById('btn-save-task-modal').addEventListener('click', () => {
      const title = document.getElementById('modal-task-title').value.trim();
      if (!title) return;

      const priority = document.getElementById('modal-priority-select').value;
      const est = document.getElementById('modal-est-select').value;
      const dateVal = document.getElementById('modal-deadline-date').value;
      const timeVal = document.getElementById('modal-deadline-time').value.trim();
      const description = document.getElementById('modal-description-input').value.trim();

      let dueFormatted = 'No due date';
      if (dateVal) {
        const d = new Date(dateVal + 'T12:00:00');
        const m = d.toLocaleDateString(undefined, { month: 'short', day: 'numeric' });
        dueFormatted = `${m} ${timeVal || '11:59 PM'}`;
      }

      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === appState.editingProjectId) || week.projects[0];

      if (proj) {
        const cleanedSubtasks = appState.modalSubtasks.filter(st => st.text.trim().length > 0);
        if (appState.editingTaskId) {
          const task = proj.tasks.find(t => t.id === appState.editingTaskId);
          if (task) {
            task.text = title;
            task.priority = priority;
            task.est = est;
            task.isoDate = dateVal;
            task.due = dueFormatted;
            task.days = [...appState.selectedModalDays];
            task.note = description;
            task.subtasks = cleanedSubtasks;
          }
        } else {
          proj.tasks.push({
            id: 't_' + Date.now(),
            text: title,
            completed: false,
            priority,
            isoDate: dateVal,
            due: dueFormatted,
            est,
            days: [...appState.selectedModalDays],
            subtasks: cleanedSubtasks,
            note: description
          });
        }
        sound.playComplete();
        saveState();
        showToast('Task saved successfully!', '💾');
      }
      closeTaskModal();
    });

    /* TASK MUTATIONS & SUBTASK TOGGLES */
    window.toggleTask = function(projectId, taskId) {
      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === projectId);
      if (proj) {
        const task = proj.tasks.find(t => t.id === taskId);
        if (task) {
          task.completed = !task.completed;
          if (task.completed) sound.playComplete();
          else sound.playTick();
          saveState();
        }
      }
    };

    window.toggleSubtaskInline = function(projectId, taskId, subtaskId) {
      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === projectId);
      if (proj) {
        const task = proj.tasks.find(t => t.id === taskId);
        if (task && task.subtasks) {
          const st = task.subtasks.find(s => s.id === subtaskId);
          if (st) {
            st.completed = !st.completed;
            sound.playTick();
            saveState();
          }
        }
      }
    };

    window.deleteTask = function(projectId, taskId) {
      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === projectId);
      if (proj) {
        proj.tasks = proj.tasks.filter(t => t.id !== taskId);
        sound.playTick();
        saveState();
        showToast('Task deleted', '🗑️');
      }
    };

    window.toggleDrawer = function(taskId) {
      const drawer = document.getElementById(`drawer-${taskId}`);
      if (drawer) {
        drawer.classList.toggle('open');
        sound.playTick();
      }
    };

    window.toggleDayAssignment = function(projectId, taskId, day) {
      const week = initCurrentWeekData();
      const proj = week.projects.find(p => p.id === projectId);
      if (proj) {
        const task = proj.tasks.find(t => t.id === taskId);
        if (task) {
          if (task.days.includes(day)) {
            task.days = task.days.filter(d => d !== day);
          } else {
            task.days.push(day);
          }
          sound.playTick();
          saveState();
        }
      }
    };

    window.deleteProject = function(projectId) {
      if (confirm("Delete this project and all its tasks?")) {
        const week = initCurrentWeekData();
        week.projects = week.projects.filter(p => p.id !== projectId);
        saveState();
        showToast('Project deleted', '🗑️');
      }
    };

    /* DRAG AND DROP CONTROLLER (MOVE MECHANIC) */
    window.handleDragStart = function(e, projId, taskId, fromDay = null) {
      appState.draggedTaskId = taskId;
      appState.draggedFromProjId = projId;
      appState.draggedFromDay = fromDay;
      e.dataTransfer.setData('text/plain', JSON.stringify({ projId, taskId, fromDay }));
      e.target.closest('.task-row-clean, .day-task-card')?.classList.add('is-dragging');
    };

    window.handleDragEnd = function(e) {
      document.querySelectorAll('.is-dragging').forEach(el => el.classList.remove('is-dragging'));
      document.querySelectorAll('.drag-over-active, .drag-hover').forEach(el => {
        el.classList.remove('drag-over-active', 'drag-hover');
      });
      appState.draggedTaskId = null;
      appState.draggedFromProjId = null;
      appState.draggedFromDay = null;
    };

    window.handleDragOver = function(e) {
      e.preventDefault();
      e.currentTarget.classList.add('drag-over-active');
    };

    window.handleDragLeave = function(e) {
      e.currentTarget.classList.remove('drag-over-active');
    };

    window.handleDropOnDay = function(e, targetDay) {
      e.preventDefault();
      e.currentTarget.classList.remove('drag-over-active');
      if (appState.draggedTaskId && appState.draggedFromProjId) {
        const week = initCurrentWeekData();
        const proj = week.projects.find(p => p.id === appState.draggedFromProjId);
        if (proj) {
          const task = proj.tasks.find(t => t.id === appState.draggedTaskId);
          if (task) {
            if (appState.draggedFromDay && appState.draggedFromDay !== targetDay) {
              task.days = task.days.filter(d => d !== appState.draggedFromDay);
            }
            if (!task.days.includes(targetDay)) {
              task.days.push(targetDay);
            }
            sound.playTick();
            saveState();
            showToast(`Task moved to ${targetDay}`, '📅');
          }
        }
      }
    };

    /* HABIT CADENCE ACTIONS */
    document.getElementById('btn-add-habit-trigger').addEventListener('click', () => {
      const title = prompt('Enter new daily habit name (e.g., Read 30m, Meditate, Zero Inbox):');
      if (title && title.trim()) {
        appState.habits.push({
          id: 'h_' + Date.now(),
          title: title.trim(),
          streak: 0,
          days: []
        });
        sound.playComplete();
        saveState();
        showToast('Habit established!', '🌱');
      }
    });

    window.toggleHabitDay = function(habitId, day) {
      const habit = appState.habits.find(h => h.id === habitId);
      if (habit) {
        if (habit.days.includes(day)) {
          habit.days = habit.days.filter(d => d !== day);
          habit.streak = Math.max(0, habit.streak - 1);
        } else {
          habit.days.push(day);
          habit.streak += 1;
        }
        sound.playTick();
        saveState();
      }
    };

    /* COMMAND PALETTE */
    const cmdBackdrop = document.getElementById('modal-cmd-palette');
    const cmdInput = document.getElementById('cmd-input');
    const cmdResults = document.getElementById('cmd-results-mount');

    function openCmdPalette() {
      cmdBackdrop.classList.add('active');
      cmdInput.value = '';
      renderCmdResults('');
      cmdInput.focus();
    }
    function closeCmdPalette() { cmdBackdrop.classList.remove('active'); }

    document.getElementById('btn-cmd-palette').addEventListener('click', openCmdPalette);
    cmdBackdrop.addEventListener('click', (e) => {
      if (e.target === cmdBackdrop) closeCmdPalette();
    });

    window.addEventListener('keydown', (e) => {
      if ((e.metaKey || e.ctrlKey) && e.key.toLowerCase() === 'k') {
        e.preventDefault();
        openCmdPalette();
      }
      if (e.key === '?' || (e.shiftKey && e.key === '/')) {
        if (!['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
          document.getElementById('modal-shortcuts').classList.toggle('active');
        }
      }
      if (e.key === ' ' && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        e.preventDefault();
        togglePomo();
      }
      if (e.key.toLowerCase() === 'a' && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        document.getElementById('btn-open-audio-modal').click();
      }
      if (e.key.toLowerCase() === 'z' && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        document.getElementById('btn-open-zen').click();
      }
      if (e.key.toLowerCase() === 's' && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        document.getElementById('btn-toggle-scratchpad').click();
      }
      if (['1', '2', '3', '4', '5', '6'].includes(e.key) && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        const map = { '1': 'board', '2': 'matrix', '3': 'habits', '4': 'calendar', '5': 'timeblock', '6': 'analytics' };
        switchView(map[e.key]);
      }
      if (e.key.toLowerCase() === 'n' && !['INPUT', 'TEXTAREA'].includes(document.activeElement.tagName)) {
        e.preventDefault();
        const week = initCurrentWeekData();
        if (week.projects.length) openTaskModal(week.projects[0].id);
      }
      if (e.key === 'Escape') {
        closeCmdPalette();
        closeTaskModal();
        closeAssistantModal();
        audioAlarmModal.classList.remove('active');
        scratchpadDrawer.classList.remove('open');
        document.getElementById('zen-focus-overlay').classList.remove('active');
        pomoPresetsPopover.classList.remove('open');
        document.getElementById('modal-new-project').classList.remove('active');
        document.getElementById('modal-shortcuts').classList.remove('active');
        document.getElementById('modal-backup').classList.remove('active');
        pastePlanModal.classList.remove('active');
      }
    });

    document.getElementById('btn-shortcuts-help').addEventListener('click', () => {
      document.getElementById('modal-shortcuts').classList.add('active');
    });

    cmdInput.addEventListener('input', (e) => renderCmdResults(e.target.value));

    function renderCmdResults(query) {
      const q = query.toLowerCase();
      const commands = [
        { label: '✨ Prompt AI Assistant', action: openAssistantModal, tag: 'AI' },
        { label: '🧘 Enter Zen Focus Mode', action: () => document.getElementById('btn-open-zen').click(), tag: 'Focus' },
        { label: '📝 Open Scratchpad Notes', action: () => document.getElementById('btn-toggle-scratchpad').click(), tag: 'Notes' },
        { label: '🎧 Audio & Alarm Panel', action: () => document.getElementById('btn-open-audio-modal').click(), tag: 'Audio' },
        { label: '💾 Backup & Export Suite', action: () => document.getElementById('btn-open-backup-modal').click(), tag: 'Data' },
        { label: '📋 Paste a Copied Plan', action: () => document.getElementById('btn-paste-plan').click(), tag: 'Import' },
        { label: 'Export Markdown Digest', action: () => document.getElementById('btn-export-markdown').click(), tag: 'Export' },
        { label: 'Toggle Grid / Split Timeline View', action: () => { appState.isTilesView = !appState.isTilesView; render(); }, tag: 'Layout' },
        { label: 'Switch to Board View', action: () => switchView('board'), tag: 'View' },
        { label: 'Switch to Eisenhower Matrix', action: () => switchView('matrix'), tag: 'View' },
        { label: 'Switch to Daily Habits Cadence', action: () => switchView('habits'), tag: 'View' },
        { label: 'Switch to Calendar View', action: () => switchView('calendar'), tag: 'View' },
        { label: 'Switch to Hourly Matrix View', action: () => switchView('timeblock'), tag: 'View' },
        { label: 'Switch to Analytics Cadence', action: () => switchView('analytics'), tag: 'View' },
        { label: 'Create New Focus Project', action: () => document.getElementById('modal-new-project').classList.add('active'), tag: 'Action' }
      ];

      const week = initCurrentWeekData();
      week.projects.forEach(p => {
        p.tasks.forEach(t => {
          commands.push({
            label: `Task: ${t.text} (${p.name})`,
            action: () => { openTaskModal(p.id, t.id); },
            tag: t.completed ? 'Done' : 'Task'
          });
        });
      });

      const filtered = commands.filter(c => c.label.toLowerCase().includes(q));
      cmdResults.innerHTML = filtered.map((c, i) => `
        <div class="cmd-item" onclick="executeCmd(${i})">
          <span>${c.label}</span>
          <span style="font-family:'JetBrains Mono'; font-size:0.7rem; color:var(--text-muted);">${c.tag}</span>
        </div>
      `).join('') || '<div style="padding:1rem; text-align:center; color:var(--text-muted); font-size:0.85rem;">No matching commands</div>';

      window._activeCmds = filtered;
    }

    window.executeCmd = function(idx) {
      if (window._activeCmds && window._activeCmds[idx]) {
        window._activeCmds[idx].action();
        closeCmdPalette();
      }
    };

    /* PERSPECTIVE NAVIGATION */
    function switchView(viewName) {
      appState.activeView = viewName;
      document.querySelectorAll('.view-btn').forEach(b => {
        b.classList.toggle('active', b.dataset.view === viewName);
      });
      document.querySelectorAll('.view-panel').forEach(p => {
        p.classList.toggle('active', p.id === `view-${viewName}`);
      });
      sound.playTick();
      render();
    }

    document.querySelectorAll('.view-btn').forEach(btn => {
      btn.addEventListener('click', () => switchView(btn.dataset.view));
    });

    /* PROJECT CREATION */
    document.getElementById('btn-add-project-modal').addEventListener('click', () => {
      document.getElementById('modal-new-project').classList.add('active');
      document.getElementById('new-project-name').focus();
    });

    document.getElementById('btn-quick-task').addEventListener('click', () => {
      const week = initCurrentWeekData();
      if (week.projects.length === 0) {
        document.getElementById('modal-new-project').classList.add('active');
      } else {
        openTaskModal(week.projects[0].id);
      }
    });

    document.getElementById('btn-cancel-proj').addEventListener('click', () => {
      document.getElementById('modal-new-project').classList.remove('active');
    });

    document.getElementById('btn-confirm-proj').addEventListener('click', () => {
      const nameInput = document.getElementById('new-project-name');
      const name = nameInput.value.trim();
      if (name) {
        const week = initCurrentWeekData();
        week.projects.push({
          id: 'p_' + Date.now(),
          name,
          subtitle: 'Workspace Module',
          tasks: []
        });
        nameInput.value = '';
        document.getElementById('modal-new-project').classList.remove('active');
        sound.playTick();
        saveState();
        showToast('Project initialized!', '🚀');
      }
    });

    /* WEEK STEPPERS */
    document.getElementById('btn-prev-week').addEventListener('click', () => {
      appState.weekOffset--;
      initCurrentWeekData();
      sound.playTick();
      render();
    });
    document.getElementById('btn-next-week').addEventListener('click', () => {
      appState.weekOffset++;
      initCurrentWeekData();
      sound.playTick();
      render();
    });

    /* FILTER HUD HANDLERS */
    document.querySelectorAll('.filter-chip').forEach(chip => {
      chip.addEventListener('click', () => {
        document.querySelectorAll('.filter-chip').forEach(c => c.classList.remove('active'));
        chip.classList.add('active');
        appState.activeFilter = chip.dataset.filter;
        render();
      });
    });

    document.getElementById('task-filter-input').addEventListener('input', (e) => {
      appState.searchQuery = e.target.value.toLowerCase();
      render();
    });

    /* CALENDAR RENDER ENGINE */
    function renderCalendar() {
      const mount = document.getElementById('cal-grid-mount');
      if (!mount) return;

      const targetMonthDate = new Date();
      targetMonthDate.setMonth(targetMonthDate.getMonth() + appState.calMonthOffset);
      const year = targetMonthDate.getFullYear();
      const month = targetMonthDate.getMonth();

      document.getElementById('cal-month-title').textContent = targetMonthDate.toLocaleDateString(undefined, { month: 'long', year: 'numeric' });

      const firstDayOfMonth = new Date(year, month, 1);
      const lastDayOfMonth = new Date(year, month + 1, 0);
      const startDayOfWeek = (firstDayOfMonth.getDay() + 6) % 7;
      const daysInMonth = lastDayOfMonth.getDate();
      const prevMonthLastDay = new Date(year, month, 0).getDate();

      const today = new Date();
      const todayISO = today.toISOString().split('T')[0];

      const allTasksByDate = {};
      Object.values(appState.weeks).forEach(w => {
        w.projects.forEach(p => {
          p.tasks.forEach(t => {
            if (t.isoDate) {
              if (!allTasksByDate[t.isoDate]) allTasksByDate[t.isoDate] = [];
              allTasksByDate[t.isoDate].push({ task: t, proj: p });
            }
          });
        });
      });

      let gridHtml = DAYS_MAP.map(d => `<div class="cal-day-heading">${d}</div>`).join('');
      let totalCells = (startDayOfWeek + daysInMonth > 35) ? 42 : 35;

      for (let i = 0; i < totalCells; i++) {
        let cellDateNum = 0;
        let isOtherMonth = false;
        let cellISODate = '';

        if (i < startDayOfWeek) {
          cellDateNum = prevMonthLastDay - (startDayOfWeek - i - 1);
          isOtherMonth = true;
          const prevM = month === 0 ? 12 : month;
          const prevY = month === 0 ? year - 1 : year;
          cellISODate = `${prevY}-${prevM.toString().padStart(2, '0')}-${cellDateNum.toString().padStart(2, '0')}`;
        } else if (i >= startDayOfWeek + daysInMonth) {
          cellDateNum = i - (startDayOfWeek + daysInMonth) + 1;
          isOtherMonth = true;
          const nextM = month === 11 ? 1 : month + 2;
          const nextY = month === 11 ? year + 1 : year;
          cellISODate = `${nextY}-${nextM.toString().padStart(2, '0')}-${cellDateNum.toString().padStart(2, '0')}`;
        } else {
          cellDateNum = i - startDayOfWeek + 1;
          cellISODate = `${year}-${(month + 1).toString().padStart(2, '0')}-${cellDateNum.toString().padStart(2, '0')}`;
        }

        const isToday = cellISODate === todayISO;
        const tasksOnDay = allTasksByDate[cellISODate] || [];

        const taskChips = tasksOnDay.map(({ task, proj }) => `
          <div class="cal-event-chip chip-${task.priority} ${task.completed ? 'chip-done' : ''}" 
            onclick="openTaskModal('${proj.id}', '${task.id}')" title="${proj.name}: ${task.text}">
            <span>${task.text}</span>
            <span style="font-family:'JetBrains Mono'; font-size:0.62rem; opacity:0.8;">${task.est || '30m'}</span>
          </div>
        `).join('');

        gridHtml += `
          <div class="cal-date-cell ${isOtherMonth ? 'other-month' : ''} ${isToday ? 'is-current-day' : ''}">
            <div class="cal-date-cell-head">
              <span class="cal-date-num">${cellDateNum}</span>
              ${tasksOnDay.length > 0 ? `<span style="font-size:0.65rem; color:var(--text-muted); font-weight:700;">${tasksOnDay.length}</span>` : ''}
            </div>
            <div style="display:flex; flex-direction:column; gap:0.25rem; overflow-y:auto; max-height:80px;">
              ${taskChips}
            </div>
          </div>
        `;
      }
      mount.innerHTML = gridHtml;
    }

    document.getElementById('btn-cal-prev').addEventListener('click', () => { appState.calMonthOffset--; sound.playTick(); renderCalendar(); });
    document.getElementById('btn-cal-next').addEventListener('click', () => { appState.calMonthOffset++; sound.playTick(); renderCalendar(); });
    document.getElementById('btn-cal-today').addEventListener('click', () => { appState.calMonthOffset = 0; sound.playTick(); renderCalendar(); });

    /* TIMEBLOCK SCHEDULE */
    window.scheduleTimeSlot = function(day, hour) {
      const week = initCurrentWeekData();
      if (!week.projects.length) return;
      const title = prompt(`Enter task name to block on ${day} at ${hour}:`);
      if (title && title.trim()) {
        week.projects[0].tasks.push({
          id: 't_' + Date.now(),
          text: title.trim(),
          completed: false,
          priority: 'med',
          isoDate: '',
          due: `${day} ${hour}`,
          est: '1h',
          days: [day],
          subtasks: [],
          note: `Time-blocked for ${hour}`
        });
        sound.playComplete();
        saveState();
        showToast(`Focus block reserved on ${day} at ${hour}`, '⏰');
      }
    };

    /* MASTER RENDER ENGINE */
    let lastCompletionRatio = 0;

    function render() {
      const week = initCurrentWeekData();
      const weekDates = getWeekDates(appState.weekOffset);
      const today = new Date();

      const boardLayout = document.getElementById('board-main-layout');
      const btnToggleTiles = document.getElementById('btn-toggle-tiles');
      if (appState.isTilesView) {
        boardLayout.classList.add('tiles-only-mode');
        btnToggleTiles.classList.add('active-toggle');
        btnToggleTiles.textContent = '⊟ SPLIT';
      } else {
        boardLayout.classList.remove('tiles-only-mode');
        btnToggleTiles.classList.remove('active-toggle');
        btnToggleTiles.textContent = '⊞ GRID';
      }

      const opt = { month: 'short', day: 'numeric' };
      document.getElementById('week-date-display').textContent = `${weekDates[0].toLocaleDateString(undefined, opt)} – ${weekDates[6].toLocaleDateString(undefined, opt)}`;
      
      const relTag = document.getElementById('week-rel-tag');
      if (appState.weekOffset === 0) relTag.textContent = 'This Week';
      else if (appState.weekOffset === -1) relTag.textContent = 'Last Week';
      else if (appState.weekOffset === 1) relTag.textContent = 'Next Week';
      else relTag.textContent = `${Math.abs(appState.weekOffset)} Weeks ${appState.weekOffset > 0 ? 'Ahead' : 'Ago'}`;

      let totalTasks = 0;
      let completedTasks = 0;
      let priorityCounts = { high: 0, med: 0, low: 0 };
      let dayCounts = { Mon: 0, Tue: 0, Wed: 0, Thu: 0, Fri: 0, Sat: 0, Sun: 0 };

      const matchesFilter = (task) => {
        if (appState.searchQuery && !task.text.toLowerCase().includes(appState.searchQuery)) return false;
        if (appState.activeFilter === 'high') return task.priority === 'high';
        if (appState.activeFilter === 'pending') return !task.completed;
        if (appState.activeFilter === 'completed') return task.completed;
        return true;
      };

      // 1. Render Project Backlog
      const projectMount = document.getElementById('project-list-mount');
      projectMount.innerHTML = week.projects.map((project, pIdx) => {
        const projTotal = project.tasks.length;
        const projCompleted = project.tasks.filter(t => t.completed).length;
        const projPct = projTotal === 0 ? 0 : Math.round((projCompleted / projTotal) * 100);

        const visibleTasks = project.tasks.filter(matchesFilter);
        const isExpanded = !!appState.expandedProjects[project.id];
        const tasksToRender = isExpanded ? visibleTasks : visibleTasks.slice(0, 3);
        const hiddenCount = Math.max(0, visibleTasks.length - 3);

        const tileIcon = TILE_ICONS[pIdx % TILE_ICONS.length];
        const tileTheme = TILE_THEMES[pIdx % TILE_THEMES.length];
        const subtitle = project.subtitle || `${projCompleted}/${projTotal} items completed`;

        const tasksHtml = tasksToRender.map(task => {
          totalTasks++;
          if (task.completed) completedTasks++;
          if (priorityCounts[task.priority] !== undefined) priorityCounts[task.priority]++;
          task.days.forEach(d => { if (dayCounts[d] !== undefined) dayCounts[d]++; });

          const daysHtml = DAYS_MAP.map(day => `
            <button class="day-toggle-chip ${task.days.includes(day) ? 'active' : ''}" 
              onclick="toggleDayAssignment('${project.id}', '${task.id}', '${day}')">${day}</button>
          `).join('');

          const dueLabel = task.due || (task.est ? `Est ${task.est}` : 'No due date');

          let subtaskPreview = '';
          if (task.subtasks && task.subtasks.length > 0) {
            const stDone = task.subtasks.filter(s => s.completed).length;
            subtaskPreview = `<span class="subtasks-meter-chip">✓ ${stDone}/${task.subtasks.length}</span>`;
          }

          return `
            <div class="task-row-clean ${task.completed ? 'completed-state' : ''}" 
              id="task-row-${task.id}"
              draggable="true"
              ondragstart="handleDragStart(event, '${project.id}', '${task.id}', null)"
              ondragend="handleDragEnd(event)">
              
              <div class="task-main-line">
                <span class="task-drag-handle" title="Drag to Day or Timeblock">⠿</span>
                <input type="checkbox" class="custom-check-box" ${task.completed ? 'checked' : ''} 
                  onchange="toggleTask('${project.id}', '${task.id}')" />
                <span class="task-title-serif" onclick="openTaskModal('${project.id}', '${task.id}')" title="Click to edit">${task.text}</span>
                <span class="tag-pill-due">${dueLabel}</span>
                <button class="btn-pin-zen" onclick="pinTaskToZen('${task.text.replace(/'/g, "\\'")}')" title="Pin to Zen Focus">🧘</button>
                <button class="btn-assign-days-trigger" onclick="toggleDrawer('${task.id}')">ASSIGN</button>
                <button class="btn-task-open-details" onclick="openTaskModal('${project.id}', '${task.id}')" title="Edit task details">→</button>
              </div>

              <div class="task-meta-subline">
                <span class="priority-badge ${task.priority}">${task.priority}</span>
                <span style="font-family:'JetBrains Mono'; font-size:0.68rem; color:var(--text-subtle);">⏱ ${task.est || '30m'}</span>
                ${subtaskPreview}
                <button class="icon-action-btn danger" onclick="deleteTask('${project.id}', '${task.id}')" title="Delete Task">✕</button>
              </div>

              ${task.subtasks && task.subtasks.length > 0 ? `
                <div class="task-subtasks-inline">
                  ${task.subtasks.map(st => `
                    <div class="subtask-item-row ${st.completed ? 'is-done' : ''}">
                      <input type="checkbox" ${st.completed ? 'checked' : ''} onchange="toggleSubtaskInline('${project.id}', '${task.id}', '${st.id}')">
                      <span>${st.text}</span>
                    </div>
                  `).join('')}
                </div>
              ` : ''}

              <div class="day-selector-drawer" id="drawer-${task.id}">
                ${daysHtml}
              </div>
            </div>
          `;
        }).join('');

        let toggleExpandHtml = '';
        if (visibleTasks.length > 3) {
          toggleExpandHtml = `
            <button class="btn-toggle-expand-tasks ${isExpanded ? 'is-expanded' : ''}" onclick="window.toggleProjectTasksExpand('${project.id}')">
              ${isExpanded ? '▴ Show Less (3)' : `▾ Show ${hiddenCount} More`}
            </button>
          `;
        }

        return `
          <div class="project-card">
            <div class="project-tile-banner">
              <div class="tile-badge-icon ${tileTheme}">${tileIcon}</div>
              <div style="flex:1; overflow:hidden;">
                <h4 style="font-weight:700; font-size:1.02rem; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; letter-spacing:-0.01em;">${project.name}</h4>
                <div style="font-size:0.75rem; color:var(--text-muted);">${subtitle}</div>
              </div>
              <div class="mini-project-progress-wrap" style="flex-direction:column; align-items:flex-end; gap:3px;">
                <span class="project-ratio-label" style="font-size:0.75rem;">${projCompleted}/${projTotal}</span>
                <div class="mini-bar-track" style="width:50px; height:4px;">
                  <div class="mini-bar-fill" style="width: ${projPct}%;"></div>
                </div>
              </div>
              <button class="icon-action-btn danger" onclick="deleteProject('${project.id}')" title="Delete Project">✕</button>
            </div>

            <div class="project-card-body">
              <div class="task-card-list">
                ${tasksHtml || '<div style="color:var(--text-subtle); font-size:0.75rem; text-align:center; padding:0.6rem 0;">No matching tasks in project</div>'}
              </div>

              <div class="project-card-footer-controls">
                <button class="btn-project-add-task-trigger" onclick="openTaskModal('${project.id}')">
                  <span>+</span> Add Task
                </button>
                ${toggleExpandHtml}
              </div>
            </div>
          </div>
        `;
      }).join('');

      // 2. Render 7-Day Matrix Columns (With Drag & Drop MOVE & Delete on Tile Top Right)
      const daysMount = document.getElementById('days-columns-mount');
      daysMount.innerHTML = DAYS_MAP.map((dayName, idx) => {
        const colDate = weekDates[idx];
        const isToday = colDate.toDateString() === today.toDateString();

        let dayTasks = [];
        week.projects.forEach(p => {
          p.tasks.filter(matchesFilter).forEach(t => {
            if (t.days.includes(dayName)) {
              dayTasks.push({ projName: p.name, projId: p.id, task: t });
            }
          });
        });

        const dayCardsHtml = dayTasks.map(item => `
          <div class="day-task-card ${item.task.completed ? 'is-done' : ''}" 
            draggable="true"
            ondragstart="handleDragStart(event, '${item.projId}', '${item.task.id}', '${dayName}')"
            ondragend="handleDragEnd(event)"
            onclick="toggleTask('${item.projId}', '${item.task.id}')">
            <div class="day-card-top">
              <span class="project-pill-label" title="${item.projName}">${item.projName}</span>
              <div class="day-card-actions">
                <span class="priority-badge ${item.task.priority}" style="font-size:0.58rem;">${item.task.priority}</span>
                <button class="btn-tile-delete" onclick="event.stopPropagation(); deleteTask('${item.projId}', '${item.task.id}')" title="Delete Task">✕</button>
              </div>
            </div>
            <span style="font-weight:600; line-height:1.25;">${item.task.text}</span>
          </div>
        `).join('');

        return `
          <div class="day-column ${isToday ? 'today-col' : ''}"
            ondragover="handleDragOver(event)"
            ondragleave="handleDragLeave(event)"
            ondrop="handleDropOnDay(event, '${dayName}')">
            <div class="day-column-head">
              <span class="day-name-tag">${dayName}</span>
              <span class="day-num-badge">${colDate.getDate()}</span>
            </div>
            <div class="day-slot-bucket">
              ${dayCardsHtml || '<div style="color:var(--text-subtle); font-size:0.72rem; text-align:center; margin-top:2.5rem;">Rest Day</div>'}
            </div>
          </div>
        `;
      }).join('');

      // 3. Render Eisenhower Decision Matrix View
      if (appState.activeView === 'matrix') {
        const matrixMount = document.getElementById('matrix-deck-mount');
        let allTasks = [];
        week.projects.forEach(p => { p.tasks.forEach(t => allTasks.push({ proj: p, task: t })); });

        const q1 = allTasks.filter(item => item.task.priority === 'high' && item.task.days.length > 0);
        const q2 = allTasks.filter(item => item.task.priority === 'high' && item.task.days.length === 0);
        const q3 = allTasks.filter(item => (item.task.priority === 'med' || item.task.priority === 'low') && item.task.days.length > 0);
        const q4 = allTasks.filter(item => item.task.priority === 'low' && item.task.days.length === 0);

        const renderQuadrantTasks = (list) => list.map(({ proj, task }) => `
          <div class="day-task-card ${task.completed ? 'is-done' : ''}" onclick="openTaskModal('${proj.id}', '${task.id}')">
            <div class="day-card-top">
              <span class="project-pill-label">${proj.name}</span>
              <button class="btn-tile-delete" onclick="event.stopPropagation(); deleteTask('${proj.id}', '${task.id}')" title="Delete Task">✕</button>
            </div>
            <span style="font-weight:600;">${task.text}</span>
          </div>
        `).join('') || '<span style="font-size:0.75rem; color:var(--text-subtle);">No tasks in quadrant</span>';

        matrixMount.innerHTML = `
          <div class="matrix-quadrant q1">
            <div class="matrix-quad-header">
              <span class="matrix-quad-title">Do First</span>
              <span class="matrix-quad-desc">Urgent & Important (${q1.length})</span>
            </div>
            ${renderQuadrantTasks(q1)}
          </div>
          <div class="matrix-quadrant q2">
            <div class="matrix-quad-header">
              <span class="matrix-quad-title">Schedule</span>
              <span class="matrix-quad-desc">Important, Not Urgent (${q2.length})</span>
            </div>
            ${renderQuadrantTasks(q2)}
          </div>
          <div class="matrix-quadrant q3">
            <div class="matrix-quad-header">
              <span class="matrix-quad-title">Delegate / Accelerate</span>
              <span class="matrix-quad-desc">Urgent, Low Impact (${q3.length})</span>
            </div>
            ${renderQuadrantTasks(q3)}
          </div>
          <div class="matrix-quadrant q4">
            <div class="matrix-quad-header">
              <span class="matrix-quad-title">Eliminate / Backlog</span>
              <span class="matrix-quad-desc">Neither (${q4.length})</span>
            </div>
            ${renderQuadrantTasks(q4)}
          </div>
        `;
      }

      // 4. Render Daily Habits View
      if (appState.activeView === 'habits') {
        const habitsMount = document.getElementById('habits-list-mount');
        habitsMount.innerHTML = appState.habits.map(h => {
          const pills = DAYS_MAP.map(d => `
            <div class="habit-check-pill ${h.days.includes(d) ? 'checked' : ''}" onclick="toggleHabitDay('${h.id}', '${d}')">
              ${d}
            </div>
          `).join('');

          return `
            <div class="habit-card">
              <div class="habit-info-group">
                <div class="habit-streak-flame">🔥 ${h.streak}</div>
                <div>
                  <h4 style="font-weight:700; font-size:1.05rem;">${h.title}</h4>
                  <span style="font-size:0.75rem; color:var(--text-muted);">${h.days.length}/7 completed this week</span>
                </div>
              </div>
              <div class="habit-days-row">
                ${pills}
              </div>
            </div>
          `;
        }).join('') || '<div style="text-align:center; color:var(--text-subtle);">No habits yet. Establish one above!</div>';
      }

      // 5. Calendar View
      if (appState.activeView === 'calendar') renderCalendar();

      // 6. Timeblock View
      if (appState.activeView === 'timeblock') {
        const timeGridMount = document.getElementById('timeblock-grid-mount');
        const hours = ['08:00', '09:00', '10:00', '11:00', '12:00', '13:00', '14:00', '15:00', '16:00', '17:00', '18:00'];
        let gridHtml = '<div></div>' + DAYS_MAP.map(d => `<div class="tb-header-cell">${d}</div>`).join('');
        
        hours.forEach(hour => {
          gridHtml += `<div class="tb-time-label">${hour}</div>`;
          DAYS_MAP.forEach(day => {
            const blockedTasks = [];
            week.projects.forEach(p => {
              p.tasks.forEach(t => {
                if (t.days.includes(day) && (t.due.includes(hour) || t.note.includes(hour))) {
                  blockedTasks.push({ proj: p, task: t });
                }
              });
            });

            const blockBadges = blockedTasks.map(b => `
              <div class="tb-event-badge" onclick="event.stopPropagation(); openTaskModal('${b.proj.id}', '${b.task.id}')">
                <span>${b.task.text}</span>
              </div>
            `).join('');

            gridHtml += `
              <div class="tb-cell" data-slot="${day}-${hour}" 
                onclick="scheduleTimeSlot('${day}', '${hour}')"
                ondragover="event.preventDefault(); this.classList.add('drag-hover');"
                ondragleave="this.classList.remove('drag-hover');"
                ondrop="event.preventDefault(); this.classList.remove('drag-hover'); handleDropOnDay(event, '${day}');">
                ${blockBadges}
              </div>
            `;
          });
        });
        timeGridMount.innerHTML = gridHtml;
      }

      // 7. Analytics View with Pure SVG Charts
      if (appState.activeView === 'analytics') {
        document.getElementById('stat-total-completed').textContent = completedTasks;
        const velocity = totalTasks ? Math.round((completedTasks / totalTasks) * 100) : 0;
        document.getElementById('stat-velocity-pct').textContent = `${velocity}%`;
        document.getElementById('stat-focus-time').textContent = `${appState.pomodoro.totalFocusMinutes}m`;

        const pTotal = (priorityCounts.high + priorityCounts.med + priorityCounts.low) || 1;
        const hPct = (priorityCounts.high / pTotal) * 100;
        const mPct = (priorityCounts.med / pTotal) * 100;

        document.getElementById('chart-priority-mount').innerHTML = `
          <svg width="120" height="120" viewBox="0 0 36 36">
            <circle cx="18" cy="18" r="15.915" fill="none" stroke="var(--border)" stroke-width="3"></circle>
            <circle cx="18" cy="18" r="15.915" fill="none" stroke="var(--accent)" stroke-width="3.8" stroke-dasharray="${hPct} ${100 - hPct}" stroke-dashoffset="25"></circle>
            <circle cx="18" cy="18" r="15.915" fill="none" stroke="var(--amber)" stroke-width="3.8" stroke-dasharray="${mPct} ${100 - mPct}" stroke-dashoffset="${25 - hPct}"></circle>
          </svg>
          <div style="font-family:'JetBrains Mono'; font-size:0.75rem; margin-left:1.5rem; display:flex; flex-direction:column; gap:0.25rem;">
            <div><span style="color:var(--accent);">■ High</span>: ${priorityCounts.high}</div>
            <div><span style="color:var(--amber);">■ Med</span>: ${priorityCounts.med}</div>
            <div><span style="color:var(--blue);">■ Low</span>: ${priorityCounts.low}</div>
          </div>
        `;

        const maxDay = Math.max(...Object.values(dayCounts), 1);
        const dayBars = DAYS_MAP.map(d => {
          const barH = (dayCounts[d] / maxDay) * 80;
          return `
            <div style="display:flex; flex-direction:column; align-items:center; gap:0.3rem; flex:1;">
              <div style="width:14px; height:80px; background:var(--bg-subtle); border-radius:4px; display:flex; align-items:flex-end;">
                <div style="width:100%; height:${barH}px; background:var(--accent); border-radius:4px;"></div>
              </div>
              <span style="font-family:'JetBrains Mono'; font-size:0.65rem; color:var(--text-muted);">${d}</span>
            </div>
          `;
        }).join('');
        document.getElementById('chart-day-mount').innerHTML = `<div style="display:flex; width:100%; gap:0.5rem; align-items:flex-end;">${dayBars}</div>`;

        const heatmapMount = document.getElementById('heatmap-grid-mount');
        let heatCells = '';
        for (let i = 0; i < 52 * 7; i++) {
          const randLevel = Math.random() > 0.6 ? `l-${Math.floor(Math.random() * 4) + 1}` : '';
          heatCells += `<div class="heatmap-cell ${randLevel}"></div>`;
        }
        heatmapMount.innerHTML = heatCells;
      }

      // 8. Master Metric & Celebration
      const pct = totalTasks === 0 ? 0 : Math.round((completedTasks / totalTasks) * 100);
      document.getElementById('master-progress-bar').style.width = `${pct}%`;
      document.getElementById('master-progress-metric').textContent = `${completedTasks}/${totalTasks} · ${pct}%`;

      if (pct === 100 && lastCompletionRatio !== 100 && totalTasks > 0) {
        launchCelebration();
        sound.playSelectedAlarm();
        showToast('All weekly tasks completed! Outstanding work!', '🏆');
      }
      lastCompletionRatio = pct;
    }

    window.toggleProjectTasksExpand = function(projectId) {
      appState.expandedProjects[projectId] = !appState.expandedProjects[projectId];
      sound.playTick();
      saveState();
    };

    document.getElementById('btn-toggle-tiles').addEventListener('click', () => {
      appState.isTilesView = !appState.isTilesView;
      sound.playTick();
      saveState();
    });

    loadState();
  </script>
</body>
</html>
