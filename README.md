# Emoji Battle Game

[▶ Play Now](https://childweii.github.io/Emoji-Battle-Game/)

**English** | [中文](README.zh-CN.md)

A tiny canvas arena where two emoji fighters auto-bounce around, pick up items, and try to knock each other to 0 HP. Mobile-friendly, no build step, just open and play.

---

## Features
- ⚔️ Auto-movement, elastic wall bounces, simple physics
- 🎁 Item spawns with clear visual effects
- ❔ Mystery button with cooldown and overlay
- 🏆 Round end screen with result & quick actions
- 📱 Responsive UI, touch friendly

---

## How to Play
1. Pick the two emoji, then **Start**.
2. Fighters move automatically and can collide. Touch items to pick them up.
3. Use the **❔** button (when visible) to roll a random power. Some powers spawn items; some trigger instantly.
4. When a player's **HP reaches 0**, the round ends and the result screen appears.

---

## Items & Effects

> Damage numbers below assume default rules (⚙️ base damage = 1). Shields, weaknesses, and other modifiers apply as described.

| Emoji | Name | Effect |
|---|---|---|
| ⚙️ | Saw | Your next collision deals **1** damage (+**1** per ⭐). Consumed on hit. Blocked by 🛡️. |
| ♥️ | Heart | Heal **+1** (up to 10). |
| 🛡️ | Shield | **10s invulnerability**: incoming damage is blocked. |
| ⏩ | Speed Up | **10s** movement speed ×2. |
| ⏪ | Slow Down | **5s** movement speed ×0.5. |
| 💔 | Break | Take **-1 HP** immediately. |
| ⭐ | Star | Stackable. Each ⭐ adds **+1** to your next ⚙️ hit. |
| 🖤 | Weaken | **10s**: you take **+1** extra damage from hits. |
| ❄️ | Freeze | **5s**: you are frozen in place (still bounce off walls). |
| 🔄 | Swap (pos) | Instantly **swap positions** of both players. |
| 💣 | Bomb | Spawns a 💥 **blast hazard**. |
| 💥 | Blast | Lives up to **10s**. Explodes when **your outer ring touches its outer ring**. On explode, **your HP is halved (ceil)**. |
| 💓 | Full Heal | Set HP to **10**. |
| ☠️ | Skull | Set HP to **3** **only if** current HP > 3 (no effect otherwise). Comes with a brief skull effect. |
| 🍻 | Beer | **Swap HP** values between both players (with a cheers effect). |
| 🌶️ | Chili (Double Reflect) | **10s exclusive buff**: other offensive pickups on you **do not take effect**; **any damage you would take is prevented and reflected back as **2×** to the attacker**. Red dashed ring while active. |
| 🕳️ | Hole | Instantly set HP to **5** and **vanish for 10s** at the same spot (no collisions or pickups). On exit, gain a **random kick velocity** so you won’t stand still. |

**Notes & interactions**
- ⚙️ base damage = 1. A hit with k ⭐ and target under 🖤 deals `1 + k + (target has 🖤 ? 1 : 0)` (unless blocked by 🛡️ or the target has 🌶️, which reflects).  
- 🌶️ is **exclusive**: while active on you, new offensive pickups (⚙️/💔/🖤/⭐ etc.) do not apply to you; incoming damage is reflected **2×**.  
- 🕳️ hides you completely: you can’t collide or pick items; blast explosions ignore you while hidden.

---

## Run Locally
- Just open `index.html` in a modern browser, or use a simple static server (e.g. VS Code Live Server).  
- No build tools required.

## Deploy (GitHub Pages)
1. Push your repo to GitHub.
2. **Settings → Pages** → Source: `main` (or your branch) / Folder: `/root` (if `index.html` is at repo root).
3. (Optional) Add a custom domain and create DNS `A`/`AAAA` records pointing to GitHub Pages.

---

## Contributing
PRs and suggestions are welcome. Please keep the game lightweight and framework-free.

## License
MIT © 2025 ChildWei
