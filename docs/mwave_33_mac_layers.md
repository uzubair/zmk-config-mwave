# mwave_33_mac Layer Reference

Source: `config/mwave_33_mac.keymap`

## Summary

| # | Name | Access |
| --- | --- | --- |
| 0 | Base | Default |
| 1 | Fn | `To Fn` key (top-right) |
| 2 | Blue | Activated externally (blue LED) |
| 3 | Green | Activated externally (green LED) |
| 4 | Symbols | `&sl 4` from right spacebar on Base |

Keys marked **none** are explicitly disabled on that layer and produce nothing.

---

## Layer 0: Base

| Area | Keys |
| --- | --- |
| Top row | `Esc`, `F1`, `F2`, `F3`, `F4`, `F5`, `F6`, `F7`, `F8`, `F9`, `F10`, `F11`, `F12`, `Home`, `End`, `Insert`, `To Fn` |
| Number row | `` ` ``, `1`–`0`, `-`, `=`, `Bksp` |
| Q row | `Tab`, `Q`, `W`, `E`, `R`, `T`, `Y`, `U`, `I`, `O`, `P`, `[`, `]`, `\`, `Del` |
| Home row | `Hyper sticky` (Caps position), `A`/Ctrl, `S`/Shift, `D`/Alt, `F`, `G`, `H`, `J`, `K`/Alt, `L`/Shift, `;`/Ctrl, `'`, `Enter`, `PgUp` |
| Bottom row | `Left Shift sticky`, `Z`, `X`, `C`, `V`, `B`, `N`, `M`, `,`, `.`, `/`, `Right Shift`, `Up`, `PgDn` |
| Bottom nav | `Left Ctrl sticky`, `Left Alt sticky`, `Left Cmd sticky`, `Space`, `Symbols (one-shot)`, `Right Cmd`, `Meh sticky`, `Right Ctrl`, `Left`, `Down`, `Right` |

### Sticky Modifiers (base layer, 1000 ms)

| Physical key | Output |
| --- | --- |
| Caps Lock position | `Hyper` — `Cmd+Shift+Alt+Ctrl` |
| Left Shift | `Left Shift` |
| Left Ctrl | `Left Ctrl` |
| Left Alt | `Left Alt` |
| Left Cmd | `Left Cmd` |
| Right Alt position | `Meh` — `Ctrl+Shift+Alt` |

### Home Row Hold-Tap (tap-preferred, 200 ms)

| Key | Tap | Hold |
| --- | --- | --- |
| `A` | `A` | `Left Ctrl` |
| `S` | `S` | `Left Shift` |
| `D` | `D` | `Left Alt` |
| `K` | `K` | `Left Alt` |
| `L` | `L` | `Left Shift` |
| `;` | `;` | `Left Ctrl` |

---

## Layer 1: Fn

Activated by the `To Fn` key (top-right on Base). Return to Base with `To Base` (same position).

| Area | Active keys | Rest |
| --- | --- | --- |
| Top row | `Mute`, `Vol Down`, `Vol Up`, `Prev`, `Play/Pause`, `Next`, `Backlight`, `Cmd+D`, `Cmd+Shift+S`, `Cmd+Tab`, `Cmd+S`, `BT`, `Scroll Lock`, `Pause`, `Num Lock`, `To Base` | — |
| Number row | `KP /`, `KP *` (positions 10–11) | none |
| Q row | `KP 7`, `KP 8`, `KP 9`, `KP -` | none |
| Home row | `Studio Unlock` (Caps position), `KP 4`, `KP 5`, `KP 6`, `KP +` | none |
| Bottom row | `Macro Version` (V position), `KP 1`, `KP 2`, `KP 3`, `KP Enter` | none |
| Bottom nav | `KP 0`, `KP .` | none |

---

## Layer 2: Blue

| Area | Active keys | Rest |
| --- | --- | --- |
| Top row | `Cmd+[`, `Cmd+]`, `Insert`, `Del`, `Cmd+Bksp`, `Num Lock`, `To Base` | none |
| Q row | `Cmd+Left`, `Play/Pause`, `Cmd+Right`, `Scroll Lock`, `Pause` | none |
| Home row | `Mute`, `Vol Down`, `Vol Up`, `F14`, `F15` | none |
| Bottom row | `Cmd+Shift+4`, `Cmd+Shift+5` | none |
| Bottom nav | `Home`, `PgDn`, `PgUp`, `End` | none |

---

## Layer 3: Green

Used for left-alt symbol shortcuts (likely app-specific bindings).

| Area | Active keys | Rest |
| --- | --- | --- |
| Q row | `Alt+5`, `Alt+4`, `Alt+3`, `Alt+2`, `Alt+1` | none |
| Home row | `Shift+Alt+H`, `Shift+Alt+L`, `Alt+H`, `Alt+L` | none |
| Bottom row | `Alt+S`, `Alt+G` | none |
| Bottom nav | `Shift+Alt+S`, `Shift+Alt+G` | none |
| Everything else | none | — |

---

## Layers 4–6: Symbols / Purple / Cyan / Yellow

Reserved. Layer 4 (Symbols) is accessible via `&sl 4` from the right spacebar on Base but has no bindings defined yet.

---

## Notes

- `&none` on any layer means the key is explicitly disabled — pressing it does nothing.
- `&sk` keys are sticky: tap once, the modifier applies to the next keypress only (1000 ms window).
- `&sl 4` is a one-shot layer: active for one keypress then returns to Base.
- `&hmt` is hold-tap: tap for the character, hold for the modifier.
