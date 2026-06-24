
# Memo-Production.com.github.az
Memo-Productionun Orginal vebsaytıdır.Buradan hamıya salamlar

[README.md](https://github.com/user-attachments/files/29288861/README.md)

# UNDERTALE GOD MODE PATCHER 🎮

A lightweight GUI tool to modify **Undertale** save files with custom player statistics.

![MemoProduction](https://img.shields.io/badge/by-MemoProduction-ff00aa?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.6%2B-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## Features ✨

- 🎯 **Modify Player Stats**: HP, ATK, DEF, GOLD, LV (LOVE), EXP, Death Count, Kill Count
- ⚡ **One-Click God Mode**: Max out all stats instantly
- 🔍 **Auto-Detect Save**: Automatically locates your Undertale save file
- 💾 **Auto-Backup**: Creates `.backup` before patching (restore anytime)
- 🎨 **Dark Retro UI**: Custom MemoProduction aesthetic (dark purple/cyan theme)
- 🌐 **Multi-Language**: UI in Azerbaijani, easy to adapt to other languages

---

## Installation

### Requirements
- Python 3.6 or higher
- `tkinter` (included with most Python installations)

### Setup
```bash
git clone https://github.com/YOUR_USERNAME/undertale-godmode-patcher.git
cd undertale-godmode-patcher
python undertale_godmode_patcher.py
```

---

## How to Use

### Step-by-Step

1. **Start Undertale** and play until you reach a save point
2. **Create or load a game** and **SAVE** (this is important!)
3. **Quit Undertale** completely
4. **Run the patcher:**
   ```bash
   python undertale_godmode_patcher.py
   ```
5. **In the GUI window:**
   - The save file should auto-detect (usually `C:\Users\YourName\AppData\Local\UNDERTALE\file0`)
   - Click **"☠ MAX GOD MODE"** for instant max stats, or
   - Manually adjust individual stats
6. Click **"▶ SAVE FAYLINA TƏTBİQ ET"** (Apply to Save File)
7. **Restart Undertale** and load your save
8. Enjoy! ✓

### Manual Save Location

If auto-detect fails, manually browse to your save file:
- **Windows:** `C:\Users\YourName\AppData\Local\UNDERTALE\file0`
- **Linux:** `~/.config/UNDERTALE/file0`
- **macOS:** `~/Library/Application Support/UNDERTALE/file0`

---

## God Mode Defaults

When you click **"☠ MAX GOD MODE"**, the following stats are applied:

| Stat | Value |
|------|-------|
| **HP** | 9999 |
| **MAX HP** | 9999 |
| **ATK** | 9999 |
| **DEF** | 9999 |
| **GOLD** | 9999 |
| **LV (LOVE)** | 20 |
| **EXP** | 99999 |
| **Death Count** | 0 |
| **Kill Count** | 0 |

You can customize any of these before applying!

---

## Troubleshooting

### "Save file not found!"
- Make sure you've **saved the game** in Undertale before running the patcher
- Manually browse to your save file using the **"AXTAR"** (Browse) button

### Game doesn't load modified save
- Check that Undertale was properly closed before patching
- Try loading a different save slot, then reload the patched save
- If all else fails, restore from backup (see below)

### How to Restore from Backup
If something goes wrong, your original save is preserved:
1. Navigate to your Undertale save folder
2. You'll see `file0.backup` (the original)
3. Delete `file0` and rename `file0.backup` to `file0`
4. Restart Undertale

---

## Customization

### Change UI Language
Edit the `labels` dictionary in the code to translate UI elements:
```python
labels = {
    "hp":     ("❤  HP (current)",    GREEN),
    "max_hp": ("❤  MAX HP",           GREEN),
    # ... etc
}
```

### Change God Mode Defaults
Modify the `GOD_VALUES` dictionary:
```python
GOD_VALUES = {
    "hp":       9999,  # Change these values
    "max_hp":   9999,
    "atk":      9999,
    # ... etc
}
```

### Change Color Scheme
Edit the MemoProduction color palette at the top:
```python
BG        = "#0a0a0f"      # Background
ACCENT    = "#c800ff"      # Main accent (purple)
ACCENT2   = "#ff00aa"      # Secondary accent (pink)
# ... etc
```

---

## Save File Format

Undertale save files are plain text, one value per line:

```
Frisk                 # Player name (line 0)
20                    # Current HP (line 1)
20                    # Max HP (line 2)
10                    # ATK (line 3)
10                    # DEF (line 4)
0                     # GOLD (line 5)
# ... more fields
```

This patcher safely modifies these values without corrupting the save structure.

---

## Known Limitations

- ✗ Cannot add items to inventory (save structure limitation)
- ✗ Cannot change room/location (would cause visual bugs)
- ✗ Cannot modify dialogue/story flags (complex GML bytecode)
- ✓ Works with all Undertale save slots (file0, file1, file2)

---

## Technical Notes

### Why Save File, Not data.win?

Undertale uses **GameMaker Studio 1.4** binary format (`data.win`). Modifying the compiled bytecode is complex and risky. Instead, this patcher modifies the save file, which is:
- ✓ Simple text format
- ✓ Safe (backed up automatically)
- ✓ Reversible
- ✓ Works cross-platform

---

## Contributing

Found a bug? Have ideas? 

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit changes (`git commit -am 'Add awesome feature'`)
4. Push to branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

MIT License — see [LICENSE](LICENSE) for details.

You are free to:
- ✓ Use commercially
- ✓ Modify
- ✓ Distribute
- ✓ Use privately

---

## Credits

**Created by:** MemoProduction  
**Inspired by:** Undertale modding community  
**Special thanks:** UndertaleModTool developers (for format documentation)

---

## Disclaimer

This tool is for **personal use only**. Undertale is owned by Toby Fox. 
This patcher does not distribute Undertale game files or code.

**Use responsibly.** 💜

---

*Last updated: June 2026*
