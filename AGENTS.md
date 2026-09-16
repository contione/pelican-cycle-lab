# Model experiment archive

- Keep this a dependency-free static HTML/SVG site that works on GitHub Pages.
- For a new model test, create a new standalone HTML file in `versions/`. Never replace an earlier experiment. Include time in the filename when the same model is tested more than once on one day.
- Label every experiment with the model specified by the user and the actual test timestamp in Asia/Shanghai (ISO 8601 with `+08:00`). Do not use the visitor's current time as the test time.
- Add the version to `versions.json` with `id`, `model`, `date`, `testedAt`, and relative `path`. Preserve old entries and their order.
- Update `index.html` to present the latest experiment, with a selector linking to every historical version. Match `VERSION_ID` to its manifest entry.
- Keep HTML, CSS, SVG, and animation code in the version HTML so each experiment remains independently inspectable.
- Verify desktop/mobile layouts, actual animation, pause/resume, speed, restart, archive links, and reduced-motion handling before publishing.
- Do not claim the displayed model label independently verifies backend model identity.
