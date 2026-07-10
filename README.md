# Ultima I on iOS

**Play Ultima I: The First Age of Darkness on your iPhone or iPad** — the complete,
original DOS game, running in DOSBox, booting straight into the game with a gem icon.

It's built on [dospad](https://github.com/litchie/dospad) (the open-source iOS DOSBox,
GPLv2), cloned and patched at build time, plus **your own** copy of Ultima I.

> **You must own Ultima I.** It isn't free, so **no game data is included in this repo** —
> the build copies your own copy onto the device. The DOSBox app is cloned + patched at
> build time, not re-hosted here.

## 📸 Screenshots

The real Ultima I, running in DOSBox — the app boots straight into it:

<p align="center">
  <img src="screenshots/title.png" width="380" alt="Ultima I title menu" />
  &nbsp;&nbsp;
  <img src="screenshots/intro.png" width="380" alt="Origin Systems intro" />
</p>

## 🚀 Install

Requires a **Mac** with **Xcode** and **git**.

**On your iPhone/iPad** (needs a free Apple ID; pass your 10-char Team ID):

```sh
git clone https://github.com/dmaynard51/ultima1-ios.git
cd ultima1-ios
dosbox/build-ios-dosbox.sh ABCDE12345
```

That's it — it clones the iOS DOSBox, patches it to auto-run Ultima I, brands it with
the gem icon and the name "Ultima I", builds, signs, installs, and copies your game
data onto the device. First run on the phone: **trust the app once** under **Settings ▸
General ▸ VPN & Device Management**, then reopen — it boots straight into the game.

By default it reads your U1 data from `/Applications/Ultima I™.app/Contents/Resources/game`
(a Mac GOG install — the **[Ultima 1+2+3 bundle](https://www.gog.com/game/ultima_123)**).
If yours is elsewhere, pass the folder (the one with `ULTIMA.EXE`) as the last argument:

```sh
dosbox/build-ios-dosbox.sh ABCDE12345 "/path/to/your/ultimaI/game"
```

(Find your Team ID: `security find-identity -v -p codesigning` — the code in parentheses.)

## 🎮 Playing

Ultima I is keyboard-driven. dospad gives you an **on-screen keyboard** and gamepad
overlay — tap the keyboard toggle to type commands. Hold the phone in **landscape**.

## ☕ Support this port

- ☕ **[Buy me a coffee (Ko-fi)](https://ko-fi.com/dmaynard)**
- 💜 **[GitHub Sponsors](https://github.com/sponsors/dmaynard51)**

## 🙏 Credits & license

- iOS DOSBox: **[dospad](https://github.com/litchie/dospad)** by litchie (GPLv2) —
  cloned + patched at build time.
- Gem app icon and the build script: MIT — see [LICENSE](LICENSE).
- *Ultima I* and its data are © Origin Systems / Electronic Arts. This project ships
  none of it; you bring your own legally-owned copy.
