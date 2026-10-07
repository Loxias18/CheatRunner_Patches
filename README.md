# CheatRunner Patches

A community collection of **PS4 & PS5 game patches** made for [CheatRunner](https://github.com/notmaj0r/CheatRunner).

Drop the patch file for your game in, launch it, and enjoy: 60 FPS, resolution unlocks, and more.

---

## 📥 Getting CheatRunner

These patches are made to work with **CheatRunner**.

You can download it here:
👉 **https://github.com/notmaj0r/CheatRunner**

---

## 📁 Repository structure

| Folder | Platform | File name |
|---|---|---|
| [`xml/`](xml) | PS4 | `CUSAXXXXX.xml` |
| [`xml_prospero/`](xml_prospero) | PS5 | `PPSAXXXXX.xml` |

Each file is named after the game's **Title ID** and can hold one or more patches for that game.

---

## 🚀 How to use

1. Download and set up [CheatRunner](https://github.com/notmaj0r/CheatRunner).
2. Find your game's Title ID (`CUSAXXXXX` for PS4, `PPSAXXXXX` for PS5).
3. Download the matching `.xml` file from the right folder (`xml` or `xml_prospero`).
4. Put it in CheatRunner's patch folder.
5. Launch the game and enable the patch you want.

> ⚠️ Patches are made for a **specific game version** (the `AppVer` field). If your game is on a different update, the patch may not work or may even crash the game.

---

## 🧩 Patch format

```xml
<?xml version="1.0" encoding="utf-8"?>
<Patch>
    <TitleID>
        <ID>CUSA00021</ID>
    </TitleID>
    <Metadata Title="Watch Dogs"
              Name="60 FPS"
              Note="Enable at game boot."
              Author="maj0r"
              PatchVer="1.0"
              AppVer="01.05"
              AppElf="eboot.bin">
        <PatchList>
            <Line Type="bytes" Address="0x1e3669b" Value="00"/>
        </PatchList>
    </Metadata>
</Patch>
```

| Field | Description |
|---|---|
| `Title` | Game name |
| `Name` | Patch name (e.g. `60 FPS`) |
| `Note` | Tips for the user (e.g. when to enable it) |
| `Author` | Credits, in order of contribution (e.g. `maj0r & Player1`) |
| `PatchVer` | Patch version |
| `AppVer` | Game update the patch was made for |
| `AppElf` | Executable that gets patched |

---

## 🤝 Contributing

Contributions are very welcome! Please read the rules below before opening a pull request.

### Pull request rules

1. **Only submit patches that are 100% tested and verified working with CheatRunner.** 
No guesses, no "should work".
2. **Filling out the form below is mandatory** in your pull request description.
3. **When editing an existing patch, never remove or overwrite the author credits, and never change their order** (order of arrival).
   Example: `maj0r & Player1 & Player2`. Add yourself at the end.

### Pull request form

Fill out this form in your PR description, using your own game's info.
This is just an example:

```
Game: God of War
Platform: PS4
TITLE ID: CUSAXXXXX
UPDATE: 1.22
Tested working with CheatRunner? Yes!
Tested on PS5? Yes
```

> `Tested working with CheatRunner?` must be **Yes**. PRs that answer anything else will not be merged.

### Checklist before you submit

- [ ] The file is in the right folder (`xml` for PS4, `xml_prospero` for PS5)
- [ ] The file is named after the Title ID
- [ ] `AppVer` matches the game update you tested on
- [ ] Existing authors are kept, in the same order
- [ ] I tested it with CheatRunner and it works
- [ ] The PR form is filled out

---

## 🙏 Credits

Thanks to everyone who tests and contributes patches.
Authors are credited inside each patch file.

---

## ⚠️ Disclaimer

Use these patches at your own risk.
Only use them with games you legally own.
This repository does not host or distribute any game files.
