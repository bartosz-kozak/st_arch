# st - my personal fork

> **Work in progress** — this is my custom build of st, actively being modified.

This is a personal fork of [st](https://st.suckless.org/) (simple terminal) by [suckless.org](https://suckless.org/). The original project is a minimal, fast, and hackable terminal emulator for X written in C.

---

## My customizations

Changes from the upstream default config:

- **Font**: changed to `MesloLGS NF` (Nerd Font), pixelsize 12, with antialiasing and autohinting enabled — for icon/glyph support matching the dwm status bar

---

## Requirements

- Xlib header files
- `MesloLGS NF` (or another Nerd Font) installed on your system

---

## Installation

Edit `config.mk` to match your local setup, then:

```sh
make clean install
```

If you did not install st with `make clean install`, compile the terminfo entry manually:

```sh
tic -sx st.info
```

---

## Key bindings (default)

| Key | Action |
|-----|--------|
| `Ctrl + Shift + Prior` | zoom in (increase font size) |
| `Ctrl + Shift + Next` | zoom out (decrease font size) |
| `Ctrl + Shift + Home` | reset zoom |
| `Ctrl + Shift + C` | copy to clipboard |
| `Ctrl + Shift + V` | paste from clipboard |
| `Ctrl + Shift + Y` | paste from primary selection |
| `Shift + Insert` | paste from primary selection |
| `Middle click` | paste from primary selection |

---

## Configuration

Edit `config.h` and recompile. st has no runtime config — all changes require a recompile:

```sh
make clean install
```

---

## License

Same as upstream st — MIT/X Consortium License. See `LICENSE` for details.

---

*Fork of [st](https://st.suckless.org/) — original author: Aurélien Aptel and suckless contributors.*
