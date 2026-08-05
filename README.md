# 💎 fxn typer

> **Native, High-Speed Auto Typer with Dark Theme UI for Windows & macOS**

`fxn typer` is a powerful, lightweight native auto-typer application built in C++ / Win32 for Windows and Objective-C++ / Cocoa for macOS. Designed for maximum speed, precision, and efficiency, it can stream keyboard input at up to **1,000,000 WPM** while automatically respecting target editor behaviors (like VS Code bracket completion and auto-closing quotes).

---

## ✨ Features

- **🚀 Ultra-High Speed Engine (Up to 100,000 WPM)**: Sub-millisecond timing precision with native OS keyboard input batching (`SendInput` on Windows, `CGEvent` on macOS).
- **🎯 3 Specialized Target Modes**:
  1. **VS Code Block Mode** *(Default)*: Automatically handles auto-paired brackets `()`, `{}`, `[]`, and quotes, using `Down-Home-Right` navigation to bypass duplicate closing characters.
  2. **VS Code Inline Mode**: Skips closing brackets/quotes using single-line `Right Arrow` navigation.
  3. **Text Editor Mode**: Pure literal typing — sends every character, space, and brace exactly as written.
- **⚡ Dynamic Delay Scaling**: Settle times for auto-complete popups and dot (`.`) escapes scale down smoothly at high WPM settings so typing never bottlenecks.
- **⌨️ Global & Local Hotkeys**: Instant control using `F5` through `F9` keys to Start, Pause, Stop, or adjust typing speed on the fly.
- **🎨 Dark Theme UI**: Sleek dark palette with electric cyan highlights, progress bar, real-time status reporting, and a signature Red Diamond `fxn` icon.
- **🛠️ Quick Toolbar**: Dedicated `Select All`, `Copy`, and `Paste` action buttons.
- **⏱️ Wait Timer & Speed Steppers**: Customizable countdown timer before typing starts, giving you time to focus your target application window.

---

## 🎹 Hotkey Reference

| Hotkey | Action | Description |
| :---: | :--- | :--- |
| **`F7`** | **Start** | Begins countdown and starts typing text into the focused window |
| **`F8`** | **Pause / Resume** | Instantly pauses or resumes the active typing worker |
| **`F9`** | **Stop** | Instantly cancels the typing job |
| **`F6`** | **Speed Up** | Increases typing speed by 25% |
| **`F5`** | **Speed Down** | Decreases typing speed by 25% |
| **`Ctrl+A` / `Cmd+A`** | **Select All** | Selects all text in the editor text box |

---

## 🚀 How to Use

1. **Paste your text** into the main `Text to type` editor box.
2. **Select your Target Mode**:
   - Use **VS Code Block** if typing C++, Python, JavaScript, or Java code into VS Code or IDEs with auto-closing brackets enabled.
   - Use **Text Editor** if typing into Notepad, TextEdit, web forms, or plain text areas.
3. **Set your desired Speed (WPM)** and **Wait Timer (sec)** *(Default: 5 seconds)*.
4. Click **▶ Start (F7)**.
5. Quickly **click into your target window** (e.g. VS Code, Notepad, Browser text area).
6. Once the countdown reaches 0, `fxn typer` will begin typing automatically into your target window.
7. Press **F8** to pause/resume or **F9** to stop at any time.

---

## 🪟 Windows Setup & Build

### Run Executable
```Double click the .exe or run this in powershell
.\auto_typer.exe
```

---

## 🍎 macOS Setup 

On macOS, keyboard automation applications require explicit system approval to send key events into other applications:

1. Open **System Settings** on your Mac.
2. Navigate to **Privacy & Security** $\rightarrow$ **Accessibility**.
3. Click **`+`** or toggle the switch to **ON** for **`auto_typer_mac`** *(or **Terminal** if running directly from Terminal)*.

```bash
./auto_typer_mac
```


## 📄 License

Distributed under the MIT License. See `LICENSE` for details.
