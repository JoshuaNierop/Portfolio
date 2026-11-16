# Portfolio — TODO

## Incomplete Features

- [ ] P2 — Planned projects afmaken: Optimization Visualizer (gradient descent 3D), Pathfinding (A*/Dijkstra/BFS)
- [ ] P2 — Mobile navigation — nav shrinkt alleen, geen hamburger menu

## Hosting

- [ ] P1 — Migratie van GitHub Pages naar Cloudflare Pages. Workspace-default is nu Cloudflare. Cloudflare Pages koppelen aan `JoshuaNierop/Portfolio`, build output leeg (static), custom domain optioneel. GitHub Pages daarna uitzetten.

## Code-audit 2026-11-17
- [x] P3 — Code-audit uitgevoerd: ongebruikte + onnodig complexe code (2026-11-17)
- [x] P2 — Verwijderd: ~17 ongebruikte methodes/getters/functies incl. legacy `_afRenderSmallBlocks` (js/projects/ai-factory.js, ~194 regels)
- [x] P2 — Verwijderd: ongebruikte `tRef` (double-pendulum.js), `pieceArea` (grid-shift.js)
- [x] P2 — Verwijderd: dode CSS voor oude chat-window en save-dialog (css/ai-factory.css, ~159 regels)
- [ ] P2 — ai-factory.js is 6400 regels in één bestand; `_openQuickEdit` (ai-factory.js:3132) is als één blok >3000 regels: opsplitsen in modules per klasse (Registry, Workspace, WindowManager, RunLog, Sidebar) — hoog risico, geen tests
- [ ] P3 — Duplicaat: ai-factory.js:3593-3608 ≈ 4599-4613; double-pendulum.js:171-181 ≈ 282-292; cart-pole.js:134-143 ≈ 228-237 — naar gedeelde helper
- [ ] P3 — Review: ~35 overige CSS-klassen in ai-factory.css lijken ongebruikt (o.a. runlog-entry*, dock-restore-btn, provider-tab, minimap-viewport) — mogelijk dynamisch opgebouwd, niet verwijderd
- [ ] P3 — Review: `matrixui.js:50 onEdit` en `wasm/build.sh` ongebruikt in code (wasm-infrastructuur, bewust laten staan?)
- [ ] P3 — Review: commentaarblok ai-factory.js (~5800, wheel=zoom overpeinzing) opruimen
