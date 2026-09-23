<div align="center">

# ⌨️ Swiss Windows Keyboard Layout for macOS

**Type on your Mac exactly like on a Swiss German Windows PC.**

<code>AltGr + 2</code> &nbsp;→&nbsp; <code>⌥ Option + 2</code> &nbsp;=&nbsp; <code>@</code>

[![License: MIT](https://img.shields.io/badge/license-MIT-22c55e?style=flat-square)](LICENSE)
[![Platform: macOS](https://img.shields.io/badge/platform-macOS-0ea5e9?style=flat-square&logo=apple&logoColor=white)](#-installation)
[![Format: .keylayout](https://img.shields.io/badge/format-.keylayout-8b5cf6?style=flat-square)](CustomSwissGerman.keylayout)
[![Layout: de-CH](https://img.shields.io/badge/layout-de--CH-f59e0b?style=flat-square)](#-key-mappings)

</div>

---

## 💡 Why

The built-in macOS "Swiss German" layout puts many characters in different places than Windows does — `@`, `#`, `|`, `\`, `[ ]` and `{ }` all move. If you switch between Windows and a Mac, or plug a PC keyboard into your Mac, that breaks your muscle memory.

This repository ships **Custom Swiss German**, a macOS keyboard layout that mirrors the Windows *German (Switzerland)* layout. The Windows **AltGr** key maps to the Mac **⌥ Option** key.

---

## 📦 What's inside

| | File | Purpose |
|:-:|:--|:--|
| ⌨️ | [`CustomSwissGerman.keylayout`](CustomSwissGerman.keylayout) | The keyboard layout definition (XML) |
| 🖼️ | [`CustomSwissGerman.icns`](CustomSwissGerman.icns) | Icon shown in the menu bar input menu |

No installer, no background process — macOS reads both files directly.

---

## 🚀 Installation

1. **Get the files** — clone the repository or download it as ZIP from GitHub:

   ```bash
   git clone https://github.com/JtheGunner/swiss-windows-keyboard-layout-macos.git
   cd swiss-windows-keyboard-layout-macos
   ```

2. **Copy both files** to the keyboard layouts folder. Pick one:

   ```bash
   # All users (requires administrator password)
   sudo cp CustomSwissGerman.keylayout CustomSwissGerman.icns "/Library/Keyboard Layouts/"

   # Current user only (no sudo)
   mkdir -p ~/Library/"Keyboard Layouts"
   cp CustomSwissGerman.keylayout CustomSwissGerman.icns ~/Library/"Keyboard Layouts/"
   ```

3. **Log out and back in** (or restart) so macOS picks up the new layout.

4. **Activate the layout**
   - Open **System Settings → Keyboard → Text Input → Input Sources → Edit…**
     <br><sub>(macOS 12 and older: **System Preferences → Keyboard → Input Sources**)</sub>
   - Click **+**, search for **Custom Swiss German** and click **Add**.
   - Select it in the input menu in the menu bar.

> [!TIP]
> Remove the built-in "Swiss German" input source afterwards, so you don't switch to it by accident with <kbd>Ctrl</kbd> + <kbd>Space</kbd>.

---

## 🔑 Key mappings

Letters, digits and the <kbd>Shift</kbd> layer (`+ " * ç % & / ( ) = ? ü è ö é ä à $ £ < >` …) match Windows. The characters you type with **AltGr** on Windows are on **⌥ Option** here:

| | Character | Windows | macOS (this layout) |
|:-:|:-:|:--|:--|
| 📧 | `@` | <kbd>AltGr</kbd> + <kbd>2</kbd> | <kbd>⌥</kbd> + <kbd>2</kbd> |
| #️⃣ | `#` | <kbd>AltGr</kbd> + <kbd>3</kbd> | <kbd>⌥</kbd> + <kbd>3</kbd> |
| 🔀 | `\|` | <kbd>AltGr</kbd> + <kbd>7</kbd> | <kbd>⌥</kbd> + <kbd>7</kbd> or <kbd>⌥</kbd> + <kbd>1</kbd> |
| ↩️ | `\` | <kbd>AltGr</kbd> + <kbd><</kbd> | <kbd>⌥</kbd> + <kbd><</kbd> |
| 🧱 | `[` `]` | <kbd>AltGr</kbd> + <kbd>ü</kbd> / <kbd>¨</kbd> | <kbd>⌥</kbd> + <kbd>ü</kbd> / <kbd>¨</kbd> |
| 🧩 | `{` `}` | <kbd>AltGr</kbd> + <kbd>ä</kbd> / <kbd>$</kbd> | <kbd>⌥</kbd> + <kbd>ä</kbd> / <kbd>$</kbd> |
| 💶 | `€` | <kbd>AltGr</kbd> + <kbd>E</kbd> | <kbd>⌥</kbd> + <kbd>E</kbd> |
| 〰️ | `~` | <kbd>AltGr</kbd> + <kbd>^</kbd> | <kbd>⌥</kbd> + <kbd>^</kbd> (dead key) or <kbd>⌥</kbd> + <kbd>N</kbd> |
| ✏️ | `´` | <kbd>AltGr</kbd> + <kbd>´</kbd> | <kbd>⌥</kbd> + <kbd>´</kbd> (dead key) |
| ➖ | `¬` `¢` | <kbd>AltGr</kbd> + <kbd>6</kbd> / <kbd>8</kbd> | <kbd>⌥</kbd> + <kbd>6</kbd> / <kbd>8</kbd> |

**Dead keys** work as on Windows: <kbd>¨</kbd>, <kbd>^</kbd>, <kbd>Shift</kbd> + <kbd>^</kbd> (`` ` ``), <kbd>⌥</kbd> + <kbd>^</kbd> (`~`) and <kbd>⌥</kbd> + <kbd>´</kbd> combine with the next letter (`^` + `e` → `ê`). Press <kbd>Space</kbd> after a dead key to type the accent on its own.

All other <kbd>⌥</kbd> and <kbd>⇧</kbd> + <kbd>⌥</kbd> combinations keep their usual macOS characters (for example <kbd>⌥</kbd> + <kbd>S</kbd> → `ß`, <kbd>⌥</kbd> + <kbd>C</kbd> → `©`). <kbd>⌘</kbd> shortcuts are unchanged.

> [!NOTE]
> On some keyboards, especially PC keyboards connected to a Mac, macOS swaps the <kbd>§</kbd> and <kbd><</kbd> keys. That is a macOS keyboard-type setting, not part of this layout — see [Troubleshooting](#-troubleshooting).

---

## 🛠️ Troubleshooting

| | Problem | Fix |
|:-:|:--|:--|
| 🔍 | Layout does not show up in the list | Check that both files are in `/Library/Keyboard Layouts/` or `~/Library/Keyboard Layouts/`, then log out and back in. |
| 🔄 | <kbd>§</kbd> and <kbd><</kbd> are swapped | Remove the keyboard type cache and re-run the Keyboard Setup Assistant: `sudo rm /Library/Preferences/com.apple.keyboardtype.plist`, then restart and choose **ISO (European)** when asked. |
| 🖼️ | Menu bar shows no icon | Make sure `CustomSwissGerman.icns` sits next to the `.keylayout` file with the same base name. |

---

## 🗑️ Uninstall

1. Remove **Custom Swiss German** in **System Settings → Keyboard → Text Input → Input Sources → Edit…**
2. Delete the files and log out:

   ```bash
   sudo rm "/Library/Keyboard Layouts/CustomSwissGerman".{keylayout,icns}
   # or, for a per-user install:
   rm ~/Library/"Keyboard Layouts/CustomSwissGerman".{keylayout,icns}
   ```

---

## 🤝 Contributing

Issues and pull requests are welcome — for example missing or wrong key mappings. To test a change, copy the edited `.keylayout` into `~/Library/Keyboard Layouts/`, log out and back in, and type the affected keys. [Ukelele](https://software.sil.org/ukelele/) is a handy visual editor for `.keylayout` files.

---

## 🙏 Credits

The layout is based on [weibeld-setup/install-keyboard-layout](https://github.com/weibeld-setup/install-keyboard-layout). Many thanks to the original project!

---

## 📄 License

[MIT](LICENSE) © Jeffry Würmli

<div align="center">
<sub>Made for everyone who switches between Windows and Mac and wants their <code>@</code> to stay where it belongs.</sub>
</div>
