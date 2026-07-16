# mwave_33_mac Layer Reference

Source: `config/mwave_33_mac.keymap`

## Summary

- `0 Base` is the typing layer.
- `1 Fn` is the function layer.
- `2 Blue` is the Mac shortcut/navigation layer.
- `3 Green` is the left-alt symbol layer.
- `4 Symbols` is a one-shot layer from the right spacebar.

## Layer 0: Base

| Area | Keys |
| --- | --- |
| Top row | `Esc`, `Mute`, `Vol Down`, `Vol Up`, `Prev`, `Play/Pause`, `Next`, `Backlight`, `F11`, `Hyper shortcut`, `Ctrl+Up`, `Cmd+Space`, `BT`, `Scroll Lock`, `Pause`, `Power`, `To Fn` |
| Number row | `` ` ``, `1` to `9`, `0`, `-`, `=`, `Bksp` |
| Q row | `Tab`, `Q`, `W`, `E`, `R`, `T`, `Y`, `U`, `I`, `O`, `P`, `[`, `]`, `\`, `Del` |
| Home row | `Caps = Hyper sticky`, `A`, `S`, `D`, `F`, `G`, `H`, `J`, `K`, `L`, `;`, `'`, `Enter`, `PgUp` |
| Bottom row | `Left Shift sticky`, `Z`, `X`, `C`, `V`, `B`, `N`, `M`, `,`, `.`, `/`, `Right Shift`, `Up`, `PgDn` |
| Thumb / nav | `Left Ctrl sticky`, `Left Alt sticky`, `Left Gui sticky`, `Space`, `Sticky Symbols`, `Right Gui`, `Meh sticky`, `Right Ctrl`, `Left`, `Down`, `Right` |

## Layer 1: Fn

| Area | Keys |
| --- | --- |
| Top row | `Transparent`, `Mute`, `Vol Down`, `Vol Up`, `Prev`, `Play/Pause`, `Next`, `Backlight`, `Cmd+D`, `Cmd+Shift+S`, `Cmd+Tab`, `Cmd+S`, `BT`, `Scroll Lock`, `Pause`, `Num Lock`, `To Base` |
| Number row | `Transparent` across the whole row except the numpad cluster |
| Q row | Numpad row starts here: `KP /`, `KP *`, and transparent placeholders |
| Home row | `Studio Unlock`, `KP 4`, `KP 5`, `KP 6`, `KP +` |
| Bottom row | `Macro Version`, `KP 1`, `KP 2`, `KP 3`, `KP Enter` |
| Thumb / nav | `KP 0`, `KP .`, remaining positions transparent |

## Layer 2: Blue

| Area | Keys |
| --- | --- |
| Top row | Mostly transparent, with `Num Lock` and `To Base` at the far right |
| Shortcut row | `Cmd+Left Bracket`, `Cmd+Right Bracket`, `Insert`, `Delete`, `Cmd+Backspace` |
| Navigation row | `Cmd+Left`, `Play/Pause`, `Cmd+Right`, `Scroll Lock`, `Pause` |
| Media row | `Mute`, `Vol Down`, `Vol Up`, `F14`, `F15` |
| Screenshot row | `Cmd+Shift+4`, `Cmd+Shift+5` |
| Thumb row | `Home`, `PgDn`, `PgUp`, `End` |

## Layer 3: Green

| Area | Keys |
| --- | --- |
| Number/symbol row | `Left Alt+5`, `Left Alt+4`, `Left Alt+3`, `Left Alt+2`, `Left Alt+1` |
| Home cluster | `Shift+Left Alt+H`, `Shift+Left Alt+L`, `Left Alt+H`, `Left Alt+L` |
| Lower cluster | `Left Alt+S`, `Left Alt+G` |
| Thumb row | `Shift+Left Alt+S`, `Shift+Left Alt+G` |
| Other positions | Transparent / disabled |

## Layer 4: Symbols

This layer is accessed from the base layer with the right spacebar using `&sl 4`.

| Area | Keys |
| --- | --- |
| Most positions | Transparent / disabled |
| Qwerty section | Symbol keys are defined here, with shifted number and punctuation mappings |

## Home Row Hold-Tap

The base layer uses a custom hold-tap behavior with:

- `200 ms` tapping term
- tap-preferred resolution

| Key | Tap | Hold |
| --- | --- | --- |
| `A` | `A` | `Left Ctrl` |
| `S` | `S` | `Left Shift` |
| `D` | `D` | `Left Alt` |
| `K` | `K` | `Left Alt` |
| `L` | `L` | `Left Shift` |
| `;` | `;` | `Left Ctrl` |

## Sticky Modifiers

The base layer also uses 1000 ms sticky keys for these modifiers:

| Key | Sticky Output |
| --- | --- |
| `Caps Lock` | `Hyper` (`Cmd + Alt + Shift + Ctrl`) |
| `Left Shift` | `Left Shift` |
| `Left Ctrl` | `Left Ctrl` |
| `Left Alt` | `Left Alt` |
| `Left Cmd` | `Left Cmd` |
| `Right Alt` | `Meh` (`Ctrl + Shift + Alt`) |

## Debounce

The keyboard config uses 5 ms debounce for both press and release.

