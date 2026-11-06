---
layout: page
title: "Crochet Projects"
permalink: https://theclarkespace.github.io/clarkespace/crochet
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mechanical Keyboard & Custom Wooden Case — Craft Studio Log</title>
    <!-- Inter Font from Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* ==========================================================================
           1. CSS VARIABLES & THEME SETUP
           ========================================================================== */
        :root {
            /* Palette: Warm Off-White Minimalist */
            --bg-primary: #fbfb9;
            --bg-surface: #ffffff;
            --bg-subtle: #f2f0ec;
            --border-color: #e5e2dc;
            --border-hover: #c9c5bd;
            
            --text-primary: #1f2022;
            --text-secondary: #595b60;
            --text-muted: #8b8d93;
            
            --accent-color: #d96b43; /* Warm Terra Cotta */
            --accent-soft: rgba(217, 107, 67, 0.1);
            --accent-hover: #be5832;
            
            --code-bg: #1e1e24;
            --code-text: #e2e8f0;

            --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            --font-mono: 'Fira Code', monospace;

            --radius-sm: 4px;
            --radius-md: 8px;
            --radius-lg: 12px;

            --transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
            --max-width-site: 1200px;
            --max-width-article: 720px;
        }

        /* Dark Mode Override */
        [data-theme="dark"] {
            --bg-primary: #121316;
            --bg-surface: #1a1c20;
            --bg-subtle: #24272e;
            --border-color: #2e323b;
            --border-hover: #454a57;
            
            --text-primary: #f0f2f5;
            --text-secondary: #a0a5b1;
            --text-muted: #6c7280;
            
            --accent-color: #e07a5f;
            --accent-soft: rgba(224, 122, 95, 0.15);
            --accent-hover: #f28b70;

            --code-bg: #0d0e11;
            --code-text: #e2e8f0;
        }

        /* ==========================================================================
           2. BASE RESETS & TYPOGRAPHY
           ========================================================================== */
        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-primary);
            font-family: var(--font-sans);
            line-height: 1.7;
            font-size: 1.05rem;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        a {
            color: var(--text-primary);
            text-decoration: underline;
            text-decoration-color: var(--border-hover);
            text-underline-offset: 4px;
            transition: var(--transition);
        }

        a:hover {
            color: var(--accent-color);
            text-decoration-color: var(--accent-color);
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
            border-radius: var(--radius-md);
        }

        /* ==========================================================================
           3. LAYOUT STRUCTURE
           ========================================================================== */
        .site-header {
            position: sticky;
            top: 0;
            background: var(--bg-primary);
            backdrop-filter: blur(8px);
            border-bottom: 1px solid var(--border-color);
            z-index: 100;
            transition: border-color 0.3s ease;
        }

        .header-inner {
            max-width: var(--max-width-site);
            margin: 0 auto;
            padding: 1rem 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand-logo {
            font-weight: 700;
            font-size: 1.15rem;
            letter-spacing: -0.02em;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .brand-logo span.badge {
            font-size: 0.75rem;
            font-weight: 500;
            background-color: var(--bg-subtle);
            color: var(--text-secondary);
            padding: 2px 6px;
            border-radius: var(--radius-sm);
            border: 1px solid var(--border-color);
        }

        .nav-group {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .nav-links {
            display: flex;
            gap: 1.25rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 500;
            color: var(--text-secondary);
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: var(--text-primary);
        }

        .theme-toggle {
            background: none;
            border: 1px solid var(--border-color);
            color: var(--text-secondary);
            padding: 0.4rem 0.6rem;
            border-radius: var(--radius-md);
            cursor: pointer;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 0.3rem;
            transition: var(--transition);
        }

        .theme-toggle:hover {
            border-color: var(--border-hover);
            color: var(--text-primary);
        }

        /* Three Column Grid Container */
        .layout-container {
            max-width: var(--max-width-site);
            margin: 0 auto;
            padding: 2.5rem 1.5rem;
            display: grid;
            grid-template-columns: 240px minmax(0, 1fr) 220px;
            gap: 3rem;
        }

        /* ==========================================================================
           4. SIDEBARS (LEFT & RIGHT)
           ========================================================================== */
        .sidebar {
            font-size: 0.9rem;
        }

        .sticky-sidebar {
            position: sticky;
            top: 5rem;
        }

        .sidebar-title {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.08em;
            color: var(--text-muted);
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .author-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            padding: 1.25rem;
            border-radius: var(--radius-md);
            margin-bottom: 2rem;
        }

        .author-avatar {
            width: 56px;
            height: 56px;
            border-radius: 50%;
            background-color: var(--bg-subtle);
            margin-bottom: 0.75rem;
            object-fit: cover;
            border: 1px solid var(--border-color);
        }

        .author-name {
            font-weight: 600;
            color: var(--text-primary);
        }

        .author-bio {
            color: var(--text-secondary);
            font-size: 0.85rem;
            margin-top: 0.25rem;
            line-height: 1.4;
        }

        .nav-tree {
            list-style: none;
        }

        .nav-tree li {
            margin-bottom: 0.5rem;
        }

        .nav-tree a {
            text-decoration: none;
            color: var(--text-secondary);
            display: block;
            padding: 0.2rem 0;
        }

        .nav-tree a:hover {
            color: var(--accent-color);
        }

        .toc-list {
            list-style: none;
            border-left: 2px solid var(--border-color);
            padding-left: 0.75rem;
        }

        .toc-list li {
            margin-bottom: 0.6rem;
        }

        .toc-list a {
            text-decoration: none;
            color: var(--text-muted);
            transition: var(--transition);
            display: block;
            font-size: 0.85rem;
            line-height: 1.3;
        }

        .toc-list a:hover {
            color: var(--text-primary);
        }

        /* ==========================================================================
           5. ARTICLE CONTENT STYLING
           ========================================================================== */
        .article-container {
            max-width: var(--max-width-article);
            margin: 0 auto;
            width: 100%;
        }

        .article-header {
            margin-bottom: 2.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid var(--border-color);
        }

        .tag-list {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
            margin-bottom: 1rem;
        }

        .tag {
            font-size: 0.75rem;
            font-family: var(--font-mono);
            background-color: var(--accent-soft);
            color: var(--accent-color);
            padding: 0.25rem 0.6rem;
            border-radius: var(--radius-sm);
            font-weight: 500;
        }

        .article-title {
            font-size: 2.5rem;
            font-weight: 700;
            line-height: 1.2;
            letter-spacing: -0.03em;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .article-meta {
            display: flex;
            gap: 1rem;
            color: var(--text-muted);
            font-size: 0.875rem;
        }

        /* Typography Inside Article Body */
        .article-body h2 {
            font-size: 1.6rem;
            margin: 2.2rem 0 1rem 0;
            letter-spacing: -0.02em;
            scroll-margin-top: 6rem;
        }

        .article-body h3 {
            font-size: 1.25rem;
            margin: 1.8rem 0 0.75rem 0;
            letter-spacing: -0.01em;
            scroll-margin-top: 6rem;
        }

        .article-body p {
            margin-bottom: 1.5rem;
            color: var(--text-secondary);
        }

        .article-body ul, 
        .article-body ol {
            margin-bottom: 1.5rem;
            padding-left: 1.5rem;
            color: var(--text-secondary);
        }

        .article-body li {
            margin-bottom: 0.4rem;
        }

        /* Blockquote Styling */
        blockquote {
            border-left: 3px solid var(--accent-color);
            padding: 0.75rem 1.25rem;
            background-color: var(--bg-surface);
            border-top-right-radius: var(--radius-md);
            border-bottom-right-radius: var(--radius-md);
            margin: 1.8rem 0;
            font-style: italic;
            color: var(--text-primary);
            border: 1px solid var(--border-color);
            border-left: 3px solid var(--accent-color);
        }

        blockquote p:last-child {
            margin-bottom: 0;
        }

        /* Image & Figure Styling */
        figure {
            margin: 2rem 0;
        }

        figcaption {
            font-size: 0.85rem;
            color: var(--text-muted);
            text-align: center;
            margin-top: 0.5rem;
            font-style: italic;
        }

        /* Specs / Callout Box */
        .callout-box {
            background-color: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-md);
            padding: 1.25rem 1.5rem;
            margin: 2rem 0;
        }

        .callout-title {
            font-weight: 600;
            font-size: 0.95rem;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--text-primary);
        }

        .callout-content {
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .callout-content ul {
            margin-bottom: 0;
            padding-left: 1.2rem;
        }

        /* Code Block Styling */
        pre {
            background-color: var(--code-bg);
            color: var(--code-text);
            padding: 1.25rem;
            border-radius: var(--radius-md);
            overflow-x: auto;
            font-family: var(--font-mono);
            font-size: 0.875rem;
            line-height: 1.5;
            margin: 1.8rem 0;
        }

        code {
            font-family: var(--font-mono);
            font-size: 0.875em;
            background-color: var(--bg-subtle);
            color: var(--accent-color);
            padding: 0.15rem 0.35rem;
            border-radius: var(--radius-sm);
        }

        pre code {
            background: none;
            color: inherit;
            padding: 0;
        }

        /* Horizontal Divider */
        hr {
            border: 0;
            height: 1px;
            background: var(--border-color);
            margin: 3rem 0;
        }

        /* ==========================================================================
           6. FOOTER STYLING
           ========================================================================== */
        .site-footer {
            border-top: 1px solid var(--border-color);
            padding: 3rem 1.5rem;
            margin-top: 4rem;
            font-size: 0.875rem;
            color: var(--text-muted);
            background-color: var(--bg-primary);
        }

        .footer-inner {
            max-width: var(--max-width-site);
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .footer-links {
            display: flex;
            gap: 1.5rem;
            list-style: none;
        }

        .footer-links a {
            color: var(--text-muted);
            text-decoration: none;
        }

        .footer-links a:hover {
            color: var(--text-primary);
        }

        /* ==========================================================================
           7. RESPONSIVE BREAKPOINTS
           ========================================================================== */
        /* Tablet: Hide right sidebar, main grid 2 cols */
        @media (max-width: 1024px) {
            .layout-container {
                grid-template-columns: 200px 1fr;
                gap: 2rem;
            }
            .right-sidebar {
                display: none;
            }
        }

        /* Mobile: Single column layout */
        @media (max-width: 768px) {
            .layout-container {
                grid-template-columns: 1fr;
                padding-top: 1.5rem;
            }

            .left-sidebar {
                order: 2; /* Move author/nav below or hide as necessary */
            }

            .article-container {
                order: 1;
            }

            .article-title {
                font-size: 1.85rem;
            }

            .header-inner {
                padding: 0.8rem 1rem;
            }

            .nav-links {
                gap: 0.8rem;
            }

            .nav-links a {
                font-size: 0.85rem;
            }

            .footer-inner {
                flex-direction: column;
                align-items: flex-start;
            }
        }
    </style>
</head>
<body>

    <!-- SITE HEADER -->
    <header class="site-header">
        <div class="header-inner">
            <a href="#" class="brand-logo">
                CLARKE STUDIO <span class="badge">MAKER</span>
            </a>
            
            <div class="nav-group">
                <nav>
                    <ul class="nav-links">
                        <li><a href="#" class="active">Projects</a></li>
                        <li><a href="#">Articles</a></li>
                        <li><a href="#">About</a></li>
                    </ul>
                </nav>
                <button class="theme-toggle" id="themeToggle" aria-label="Toggle dark/light theme">
                    <span id="themeIcon">🌙</span>
                </button>
            </div>
        </div>
    </header>

    <!-- MAIN THREE-COLUMN LAYOUT -->
    <div class="layout-container">
        
        <!-- LEFT SIDEBAR: Author Info & Project Nav -->
        <aside class="sidebar left-sidebar">
            <div class="sticky-sidebar">
                <div class="author-card">
                    <img src="https://placehold.co/100x100/e5e2dc/1f2022?text=AC" alt="Alex Clarke" class="author-avatar" onerror="this.src='https://via.placeholder.com/100'">
                    <div class="author-name">Alex Clarke</div>
                    <p class="author-bio">Hardware tinkerer, woodworker, and embedded software engineer.</p>
                </div>

                <div class="sidebar-title">Recent Build Logs</div>
                <ul class="nav-tree">
                    <li><a href="#">• CNC Walnut Keyboard Case</a></li>
                    <li><a href="#">• Custom LoRa Weather Node</a></li>
                    <li><a href="#">• Minimal Leather Sleeve</a></li>
                    <li><a href="#">• Desk Lamp PWM Dimmer</a></li>
                </ul>
            </div>
        </aside>

        <!-- CENTER ARTICLE CONTENT -->
        <main class="article-container">
            <article>
                <header class="article-header">
                    <div class="tag-list">
                        <span class="tag">#Electronics</span>
                        <span class="tag">#Woodworking</span>
                        <span class="tag">#CAD</span>
                    </div>
                    <h1 class="article-title">Crafting a Custom CNC Walnut Case for a 65% Mechanical Keyboard</h1>
                    <div class="article-meta">
                        <span>October 24, 2026</span>
                        <span>•</span>
                        <span>8 min read</span>
                    </div>
                </header>

                <div class="article-body">
                    <p>
                        Building a custom mechanical keyboard from scratch provides a unique intersection of tactile software design, mechanical tolerances, and woodworking. For this build, I wanted to replace a standard aluminum tray-mount case with a solid walnut enclosure crafted using a desktop CNC router.
                    </p>

                    <h2 id="design-phase">1. Design & CAD Modeling</h2>
                    <p>
                        The goal was a seamless design with brass threaded inserts and a subtle 6-degree typing angle. I started in Fusion 360 by importing standard PCB dimensions for the 65% layout and creating offset bounds for the walnut shell.
                    </p>
                    
                    <blockquote>
                        <p>"Always budget an additional 0.3mm of clearance around the inner perimeter when working with hardwood; thermal expansion and finish coats will tighten tolerances quickly."</p>
                    </blockquote>

                    <!-- CALLOUT SPECIFICATION BOX -->
                    <div class="callout-box">
                        <div class="callout-title">
                            🛠 Project Specifications
                        </div>
                        <div class="callout-content">
                            <ul>
                                <li><strong>Material:</strong> Kiln-dried American Black Walnut</li>
                                <li><strong>Finish:</strong> Hardwax oil (Rubio Monocoat 2C)</li>
                                <li><strong>Mounting:</strong> Gasket mount with silicone strips</li>
                                <li><strong>Microcontroller:</strong> RP2040 running QMK Firmware</li>
                            </ul>
                        </div>
                    </div>

                    <h2 id="machining-process">2. Machining & Toolpaths</h2>
                    <p>
                        Roughing was executed using a 1/4" 2-flute flat endmill at 12,000 RPM. Finishing passes around the exterior curves were finished with a 1/8" ball nose bit for smooth transitions.
                    </p>

                    <!-- PLACEHOLDER FIGURE WITH CAPTION -->
                    <figure>
                        <img src="https://placehold.co/800x450/f2f0ec/595b60?text=CNC+Machining+Pass+Photo" alt="CNC machining walnut block">
                        <figcaption>Figure 1: Roughing pass clearance inside the switch pocket chamber.</figcaption>
                    </figure>

                    <p>
                        The trickiest part was pocketing out space for the USB-C daughterboard. Below is the simplified pin map used in the custom QMK configuration:
                    </p>

                    <!-- CODE SAMPLE -->
<pre><code>// QMK Matrix Configuration Snippet
#define MATRIX_ROWS 5
#define MATRIX_COLS 16

const uint8_t row_pins[MATRIX_ROWS] = { GP0, GP1, GP2, GP3, GP4 };
const uint8_t col_pins[MATRIX_COLS] = { 
    GP5, GP6, GP7, GP8, GP9, GP10, GP11, GP12, 
    GP13, GP14, GP15, GP16, GP17, GP18, GP19, GP20 
};</code></pre>

                    <h2 id="finishing-assembly">3. Sanding & Hardwax Finishing</h2>
                    <p>
                        After popping the case out of the stock tab anchors, sanding proceeded through 120, 180, 240, and 320 grits. A single coat of natural hardwax oil was buffed into the grain, bringing out deep chocolate tones while preserving natural wood texture.
                    </p>

                    <h2 id="reflection">Key Takeaways & Lessons</h2>
                    <ul>
                        <li><strong>Dust Collection:</strong> Fine walnut dust clogs linear rails quickly; run vacuum hoods at maximum flow.</li>
                        <li><strong>Thread Inserts:</strong> Heat-set M2 inserts work surprisingly well in dense hardwood if pre-drilled to exact outer shank diameters.</li>
                    </ul>
                </div>
            </article>
        </main>

        <!-- RIGHT SIDEBAR: Table of Contents -->
        <aside class="sidebar right-sidebar">
            <div class="sticky-sidebar">
                <div class="sidebar-title">On This Page</div>
                <ul class="toc-list">
                    <li><a href="#design-phase">1. Design & CAD</a></li>
                    <li><a href="#machining-process">2. Machining Pass</a></li>
                    <li><a href="#finishing-assembly">3. Hardwax Finish</a></li>
                    <li><a href="#reflection">Lessons Learned</a></li>
                </ul>
            </div>
        </aside>

    </div>

    <!-- SITE FOOTER -->
    <footer class="site-footer">
        <div class="footer-inner">
            <div>
                © 2026 Alex Clarke. Built for GitHub Pages.
            </div>
            <ul class="footer-links">
                <li><a href="#">GitHub Repository</a></li>
                <li><a href="#">RSS Feed</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
    </footer>

    <!-- LIGHT / DARK MODE SCRIPT -->
    <script>
        const themeToggleBtn = document.getElementById('themeToggle');
        const themeIcon = document.getElementById('themeIcon');

        // Check stored theme preference or systemic setting
        const savedTheme = localStorage.getItem('theme');
        const systemPrefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

        if (savedTheme === 'dark' || (!savedTheme && systemPrefersDark)) {
            document.documentElement.setAttribute('data-theme', 'dark');
            themeIcon.textContent = '☀️';
        } else {
            document.documentElement.setAttribute('data-theme', 'light');
            themeIcon.textContent = '🌙';
        }

        themeToggleBtn.addEventListener('click', () => {
            const currentTheme = document.documentElement.getAttribute('data-theme');
            let newTheme = 'light';

            if (currentTheme === 'light') {
                newTheme = 'dark';
                themeIcon.textContent = '☀️';
            } else {
                themeIcon.textContent = '🌙';
            }

            document.documentElement.setAttribute('data-theme', newTheme);
            localStorage.setItem('theme', newTheme);
        });
    </script>
</body>
</html>
