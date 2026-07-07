Yves.OS

A browser-based operating system experiment I built from scratch using only plain HTML, CSS, and JavaScript—no frameworks attached.

<img width="1440" height="900" alt="Screenshot 2026-07-07 at 12 09 34 PM" src="https://github.com/user-attachments/assets/7c23d517-e6a9-403a-ac2e-93138fa2de81" />

Try Yves.OS Live Right Here: https://kingpushkingpinoverlord.github.io/Yves.OS/

Quick Start

Want to poke around? It is straightforward. You don't need to install anything.

Just click the live link above, or if you downloaded the code:

Open the folder.

Double-click index.html to open it in your browser.

Features

I tried to pack in as many tools as I could while keeping it lightweight:

Real Window Management: Drag, maximize, and close app windows with macOS-style controls.

Dynamic Glass UI: Uses a frosted glass aesthetic with an interactive dock and animated backgrounds.

Notion-style Workspace: A mini rich-text editor for jotting down your ideas.

Project Tracker: An organized to-do list that tracks your progress.

Focus Timer: A built-in Pomodoro timer.

Live Customization: Open the Settings app to tweak blur, saturation, and background colors in real-time.

Flappy Break Time: A fully playable Flappy Bird clone.

Terminal & Easter Eggs: A functional command line. Type help to explore, or try hidden commands like matrix or lucy for ASCII art surprises.

How to run it locally

I wanted to keep this project completely self-contained. There are no build tools, no Node.js dependencies, and no package managers required.

To run it locally:

Clone or download this repository.

Open the index.html file directly in Chrome, Firefox, Safari, or Edge.

How it works

I built Yves.OS to see how far I could push vanilla web technologies without reaching for libraries like React or Vue. Here is the magic under the hood:

The Interface: The entire UI relies on native CSS3. The frosted glass effect uses backdrop-filter: blur(). When you change a color in the Settings app, JavaScript updates global CSS variables (:root) to change the theme instantly.

The Background Engine: That ambient, glowing background is a native HTML5 <canvas> element continuously drawing overlapping circles with blur filters applied in real-time via a requestAnimationFrame loop.

State Management: Window states are managed through simple JavaScript objects and DOM manipulation. Clicking an app on the dock injects an HTML template into the page and attaches drag listeners.

The Game: The Flappy Bird clone manipulates the absolute positioning of DOM elements (divs for the bird and pipes) using a physics loop synced to the browser's refresh rate.
