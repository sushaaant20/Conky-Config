# 💻 Minimalis Conky 1.4 Professional

**Author:** Sushant
**Release Date:** 10 June 2025
**Tested On:** Linux Mint 22.1 Xia

Minimalis Conky 1.4 is a sleek, professional-grade Conky configuration crafted for clarity, performance, and aesthetic simplicity. Designed for system monitoring enthusiasts, it offers essential real-time stats with smooth visuals and clean formatting — no distractions, no clutter.

---

## ✨ Features

* 🧠 **System Info:** Hostname, OS, Kernel, Uptime, Load Average
* 🖥️ **CPU Monitoring:** Model, Core Usage, Per-Core Stats with smart color-coded load bars
* 🌡️ **Temperature Readings:** Individual core temp and average calculation
* 🧮 **Memory & Swap Usage:** Dynamic, color-coded usage bars
* 📦 **Storage Insight:** Root and Home partitions with real-time read/write I/O
* 🌐 **Network Stats:** Interface name, IP, SSID, up/down speed (in MB/s), total data used (in MB)
* ⚙️ **Top Processes:** CPU and Memory-heavy apps sorted and listed
* 🎯 **Performance Optimized:** Uses sample averaging and smooth rendering with zero lag

---

## 📸 Screenshots
![Conky](https://github.com/user-attachments/assets/2b520d64-e139-49cf-98ee-e42e72d4bbb7)
![Screenshot from 2025-06-10 20-04-34](https://github.com/user-attachments/assets/e1b21c7f-93e1-483b-bb72-70c94b0c00cf)

---

## 🛠️ Installation

### 1. Install Dependencies

```bash
sudo apt install conky-all lm-sensors bc fonts-roboto fonts-roboto-mono
# or on Fedora:
# sudo dnf install conky lm_sensors google-roboto-fonts bc
```

Then, detect available sensors:

```bash
sudo sensors-detect
```

Follow prompts and reboot if required.

---

### 2. Clone This Repository

```bash
git clone https://github.com/yourusername/minimalis-conky
cd minimalis-conky
```

---

### 3. Install Fonts

```bash
mkdir -p ~/.local/share/fonts
cp ConkySymbols.ttf ~/.local/share/fonts/
fc-cache -fv
```

---

### 4. Apply Conky Configuration

```bash
cp conky.conf ~/.conkyrc
conky &
```

---

## ⚙️ Customization

* 🔌 **Network Interface:**
  Replace `wlx503eaa7a1b6f` in the config with your actual interface name (use `ip a` to check).

* 🎨 **Colors:**
  Edit `color1`, `color2`, and `color3` in the config to match your theme or wallpaper.

* 🧭 **Positioning:**
  Tweak `alignment`, `gap_x`, and `gap_y` in the `.conkyrc` to place the widget wherever you want.

* 🔤 **Font Styling:**
  Make sure `Roboto Mono` and `ConkySymbols.ttf` are properly installed — otherwise icons and layout might break.

---

## 🧩 Compatibility Notes

* 🖼️ Designed for **X11-based** window managers (Cinnamon, XFCE, MATE, Openbox, etc.)
* 🧠 Sensor output may vary by hardware. If CPU temps don’t show, adjust the `sensors` line in the config (e.g., replace `"Core 0"` with `"Package id 0"` or check output of `sensors`)
* 🐧 Works on **Ubuntu, Debian, Fedora, and Arch** with minor tweaks

---

## 📜 License

This project is licensed under the **MIT License**.
Feel free to **fork, modify, improve, or distribute** it — credit appreciated but not required.

---

## 🙏 Credits
Crafted with 💙 by **Sushant**
