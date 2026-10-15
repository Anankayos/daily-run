# Daily Run

A one-page study tracker: today's blocks, ticks, XP, streak, course counters and coach notes. It is a single static `index.html`, served by GitHub Pages.

The page holds no data. On each device it asks once for a GitHub username, the private data repo (`daily-run-data`) and a fine-grained token with **Contents: Read and write** on that repo only. The token is stored in that browser's local storage and sent only to `api.github.com`.

Ticks show at once and are saved to the data repo as one commit per change. If the connection drops, changes wait on the device and go up when it comes back. The page checks the repo for new coach notes every 45 seconds and whenever you return to the tab.
