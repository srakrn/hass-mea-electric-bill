# Repository workflow

- Use `main` as the trunk and the base for pull requests. Start each change from the latest `origin/main` on a short-lived branch such as `feature/solar-export` or `fix/export-history`.
- Keep each pull request focused. Merge through a pull request after the **Card checks** job passes, then remove the merged feature branch.
- Run `node --check mea-electric-bill-card.js` and `node --test` before pushing. The tests use the built-in Node.js test runner and work without a Home Assistant instance or npm packages. CI uses Node.js 24.
- When changing energy calculations, exercise the card with Recorder statistics and raw history. Keep grid import, grid export, and solar self-consumption independent, and cover existing configurations that omit optional entities.

## Design and copy

Keep the card and editor uncluttered. Add text when it helps the user understand, configure, or operate the card.
