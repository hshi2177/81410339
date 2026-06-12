# 81410339
作業
[AGENTS.md](https://github.com/user-attachments/files/28875190/AGENTS.md)
# AGENTS.md

Single-file children's game learning website (`index.html`), Traditional Chinese (繁體中文).

## Structure

- `index.html` — self-contained single HTML file with embedded CSS and JS
- No build tooling, runtime, or dependencies. Open directly in a browser.

## Games

| # | Game | Win condition |
|---|------|--------------|
| 1 | 龜兔賽跑 (Tortoise & Hare) | Click/tap the track to make the hare run; don't let it sleep or the tortoise wins |
| 2 | 記憶動物翻牌 (Memory) | Match all 8 animal pairs in a 4×4 grid |
| 3 | 形狀顏色連連看 (Shapes & Colors) | Match all 8 shape-and-color pairs in a 4×4 grid |

## Behavior

- **Winning**: fireworks particle effect (canvas overlay) + celebration modal with "再玩一次" / "回到首頁"
- **Tortoise wins**: game-over overlay, same retry options, no fireworks
- All state is in-memory; refreshing the page resets everything

## File layout

- `index.html` at root — the only source file
- `AGENTS.md` — this file

## Key implementation details

- Pages: show/hide via CSS classes (`.active`), no router
- Tortoise & Hare: DOM-based with `requestAnimationFrame` loop for progress
- Memory: DOM-based, CSS 3D perspective flip animation
- Shapes & Colors: DOM grid, matched tiles fade out with scale animation
- Fireworks: secondary canvas overlaid on `#celebration`, burst + particle physics
