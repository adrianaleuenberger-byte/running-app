# RunWise calendar, cross-training and run rescheduling

- **Intent:** Extend the existing single-file RunWise calendar so a runner can align planned sessions with long-run preferences, race distance, other sport activities, and calendar changes.
- **Approach:** Update the existing standalone `index.html` on `main`; do not introduce a framework or build step. This preserves the current GitHub Pages setup and browser-local storage model.
- **Features:** Add a 10-mile (16 km) goal alongside 10K; store the preferred long-run weekday; let users reserve future dates for another sport (name, duration, notes) and keep generated runs off those dates; make planned runs movable by drag-and-drop with a date-picker fallback; include other-sport data in export/import and clear-all.
- **Conflict handling:** Do not create or move a planned run onto a logged run, another plan, an other-sport block, or race day. A sport block cannot be saved over a planned run; move/remove the run first.
- **Non-goals:** No backend, cross-device sync, Strava integration, or guarantee of race performance.
- **Deployment:** Commit the updated `index.html` and this design note to `main`; verify the GitHub Pages site after push.
