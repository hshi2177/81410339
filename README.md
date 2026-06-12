# 81410339
作業
# 🎮 兒童遊戲學習樂園

三個適合兒童的網頁小遊戲，**繁體中文**，單一 HTML 檔，開瀏覽器就能玩。

## 遊戲

| 遊戲 | 玩法 | 過關條件 |
|------|------|---------|
| 🐢 龜兔賽跑 | 點擊/觸碰賽道讓兔子跑；別讓兔子睡著 | 兔子比烏龜先到終點 |
| 🧠 記憶動物翻牌 | 4×4 牌陣，翻牌配對動物 | 湊齊 8 對 |
| 🔵 形狀顏色連連看 | 4×4 網格中找出相同形狀與顏色的配對 | 湊齊 8 對 |

## 怎麼用

直接雙擊 `index.html` 在瀏覽器開啟即可，不需安裝任何東西。

## 系統需求

任何現代瀏覽器（Chrome、Firefox、Safari、Edge）。
[README.md](https://github.com/user-attachments/files/28875325/README.md)

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
[index.zip](https://github.com/user-attachments/files/28875329/index.zip)
