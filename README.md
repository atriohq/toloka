# Toloka OS

**Toloka** is a friendly, lightweight Linux distribution based on Debian Trixie.  
It uses KDE Plasma 6 and includes all the essentials — browser, office, media player, and more — right out of the box.

Whether you're a beginner or a power user, Toloka is made to just work.

## Highlights

- 🖥️ Clean and modern KDE Plasma 6 desktop
- 📦 Based on stable Debian Trixie (Testing)
- 🌐 Comes with Firefox, LibreOffice, VLC, and more
- 🎧 Full audio/video support with firmware and codecs
- 🧰 Calamares installer for easy setup
- 💻 Live boot support (USB or DVD)

---

## 🔧 Build Instructions

You can build Toloka on any Debian or Ubuntu-based machine or VM:

### 1. Install live-build and required tools:

```bash
sudo apt update
sudo apt install live-build git
```

### 2. Clone the Toloka build repo:

```bash
git clone https://github.com/atriohq/toloka.git
cd toloka
```

### 3. Clean previous builds (if any):

```bash
sudo lb clean --all
```

### 4. Configure the build:

```bash
sudo lb config \
  --distribution trixie \
  --archive-areas "main contrib non-free non-free-firmware" \
  --bootappend-live "boot=live components quiet splash" \
  --binary-images iso-hybrid
```

### 5. Build the ISO:

```bash
sudo lb build
```

## 📦 Where to find the ISO

After the build completes successfully, the ISO will be located in:

```bash
./live-image-amd64.hybrid.iso
```

You can write it to a USB stick with `dd` or use any USB image writer tool.

## 📜 License

Toloka is released under the GNU GPL v3 or later.

## ❤️ Toloka is for everyone.

Simple. Beautiful. Powerful.