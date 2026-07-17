# mwave_33_mac Layer Reference

Source: `config/mwave_33_mac.keymap`

## Summary

| # | Name | Access |
| --- | --- | --- |
| 0 | Base | Default |
| 1 | Fn | `To Fn` key (top-right) or `lsl 1` (tap=one-shot, hold=momentary) |
| 2 | Blue | Activated externally (blue LED) |
| 3 | Green | Activated externally (green LED) |
| 4 | Symbols | `lsl 4` (tap=one-shot, hold=momentary) |

Keys marked **none** are explicitly disabled on that layer and produce nothing.

---

## Layer 0: Base

| Area | Keys |
| --- | --- |
| Top row | `Esc`, `F1`–`F12`, `Home`, `End`, `Insert`, `To Fn` |
| Number row | `` ` ``, `1`–`0`, `-`, `=`, `Bksp` |
| Q row | `Tab`, `Q`, `W`, `E`, `R`, `T`, `Y`, `U`, `I`, `O`, `P`, `[`, `]`, `\`, `Del` |
| Home row | `Hyper sticky`, `A`/Ctrl, `S`/Shift, `D`/Alt, `F`, `G`, `H`, `J`, `K`/Alt, `L`/Shift, `;`/Ctrl, `'`, `Enter`, `PgUp` |
| Bottom row | `Left Shift sticky`, `Z`, `X`, `C`, `V`/Meh, `B`, `N`, `M`/Meh, `,`, `.`, `/`, `Right Shift`, `Up`, `PgDn` |
| Bottom nav | `Left Ctrl sticky`, `Left Alt sticky`, `Left Cmd sticky`, `Space`, `Right Space`/Cmd+Space, `Symbols lsl`, `Fn lsl`, `Right Ctrl`, `Left`, `Down`, `Right` |

### Sticky Modifiers (1000 ms)

| Physical key | Output |
| --- | --- |
| Caps Lock position | `Hyper` — `Cmd+Shift+Alt+Ctrl` (sticky) |
| Left Shift | `Left Shift` (sticky) |
| Left Ctrl | `Left Ctrl` (sticky) |
| Left Alt | `Left Alt` (sticky) |
| Left Cmd | `Left Cmd` (sticky) |

### Home Row Hold-Tap — `hmt` (tap-preferred, 200 ms)

| Key | Tap | Hold |
| --- | --- | --- |
| `A` | `A` | `Left Ctrl` |
| `S` | `S` | `Left Shift` |
| `D` | `D` | `Left Alt` |
| `K` | `K` | `Left Alt` |
| `L` | `L` | `Left Shift` |
| `;` | `;` | `Left Ctrl` |

### Other Hold-Tap Keys — `hmt` (tap-preferred, 200 ms)

| Key | Tap | Hold |
| --- | --- | --- |
| `V` | `V` | `Meh` — `Ctrl+Shift+Alt` |
| `M` | `M` | `Meh` — `Ctrl+Shift+Alt` |
| Right Space | `Ctrl+Space` | `Cmd+Space` |

### Layer Access Keys — `lsl` (tap-preferred, 200 ms)

| Physical key | Tap | Hold |
| --- | --- | --- |
| ralt position | One-shot Symbols (layer 4) | Momentary Symbols (layer 4) |
| beside ralt | One-shot Fn (layer 1) | Momentary Fn (layer 1) |

---

## Layer 1: Fn

Activated by `To Fn` (top-right on Base) or via `lsl 1` key. Return to Base with `To Base` (same position).

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

Used for left-alt symbol shortcuts (app-specific bindings).

| Area | Active keys | Rest |
| --- | --- | --- |
| Q row | `Alt+5`, `Alt+4`, `Alt+3`, `Alt+2`, `Alt+1` | none |
| Home row | `Shift+Alt+H`, `Shift+Alt+L`, `Alt+H`, `Alt+L` | none |
| Bottom row | `Alt+S`, `Alt+G` | none |
| Bottom nav | `Shift+Alt+S`, `Shift+Alt+G` | none |
| Everything else | none | — |

---

## Layer 4: Symbols

Accessed via the `lsl 4` key (tap=one-shot, hold=momentary). Only the QWERTY section (Q–P, A–;, Z–/) has active keys, mirroring the Voyager symbol layer layout.

```
Q   W   E   R   T       Y   U   I   O   P
!   @   #   )   $       `   (   -   +   \

A   S   D   F   G       H   J   K   L   ;
~   /   ^   }   =       '   {   -   *   :

Z   X   C   V   B       N   M   ,   .   /
_   |   >   ]   &       "   [   <   %   ?
```

> Z (bottom-left) is `none` — no symbol assigned there.

---

## Layers 5–7: Purple / Cyan / Yellow

Reserved, no bindings defined.

---

## Notes

- `&none` = key is explicitly disabled; pressing it does nothing.
- `&sk` = sticky key: tap once, the modifier applies to the next keypress only (1000 ms window).
- `&sl` = one-shot layer: active for one keypress then returns to Base.
- `&mo` = momentary layer: active while the key is held.
- `&lsl` = custom hold-tap: tap for one-shot layer (`&sl`), hold for momentary layer (`&mo`).
- `&hmt` = custom hold-tap: tap for character, hold for modifier (tap-preferred, 200 ms).
- `&to` = permanent layer switch (used for Base ↔ Fn toggle).
