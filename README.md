# Pi-hole Virtual Switch for Hubitat

This is an enhanced version of the **Pi-hole Virtual Switch** for Hubitat, originally created by [Nick Veenstra](https://github.com/jedbro/Hubitat-Projects), with contributions from **cuboy29, harriscd, and Jed Brown**. This driver allows you to control your Pi-hole instance from Hubitat, enabling on/off toggling, status checks, and automation integration.

## 🚀 Features

- ✅ Enable or disable Pi-hole via a virtual switch in Hubitat.
- 🔄 Check the current status of Pi-hole.
- ⚡ **Updated to comply with Pi-hole v6 API changes.**
- 📦 **Now installable via [Hubitat Package Manager (HPM)](https://github.com/HubitatCommunity/hubitatpackagemanager).**
- 🛠️ Improved code structure, better logging, and added authentication handling.

## 🔄 Why This Version?

With the release of **Pi-hole v6**, the API structure changed, requiring updates to the original driver. This version ensures compatibility with the latest Pi-hole release while improving maintainability, security, and performance.

## 📦 Installation

### **Hubitat Package Manager (Recommended)**
1. Open **Hubitat Package Manager** in your Hubitat interface.
2. Choose **Install** → **Search by Keywords**.
3. Search for **Pi-hole Virtual Switch**.
4. Click **Install** and follow the on-screen instructions.

### **Manual Installation**
1. Open **Hubitat Web Interface** → **Drivers Code**.
2. Click **+ New Driver** and paste the contents of [`pi-hole-virtual-switch.groovy`](https://raw.githubusercontent.com/walksonair/Hubitat-Pi-hole-Virtual-Switch/refs/heads/main/pi-hole-virtual-switch.groovy).
3. Save the driver.
4. Go to **Devices** → **Add Virtual Device** and select **Pi-hole Virtual Switch** as the driver.

## ⚙️ Configuration
1. After installing, open the device page in Hubitat.
2. Enter your **Pi-hole API key** and **server URL** in the device preferences.
3. Save the settings.
4. Use Hubitat automation or dashboards to toggle Pi-hole on/off.

## 🔄 Updates
To update the driver via HPM:
1. Open **Hubitat Package Manager**.
2. Select **Update** → **Check for Updates**.
3. If an update is available, follow the instructions to install.


## 🆕 Release Notes

### v6.0.1 - 2025-05-17

- Added calls to `unschedule()` and `unsubscribe()` at the start of `initialize()` to clear existing schedules and subscriptions.
- Introduced `unschedule("updateBlockingResumeTime")` in `handleOnResponse` to remove stale resume-time schedules when re-enabling blocking.

## 🏆 Credits

This project is based on the original [Pi-hole Virtual Switch](https://github.com/jedbro/Hubitat-Projects/blob/main/Pi-Hole%20Virtual%20Switch/pi-hole-virtual-switch.groovy) by **Nick Veenstra, cuboy29, harriscd, and [Jed Brown](https://github.com/jedbro)**. 

**Major updates for Pi-hole v6 compatibility and HPM support were made by [WalksOnAir](https://github.com/WalksOnAir).**

### ❤️ Buy Me a Beer (or Coffee!)

I'm a single papa raising two amazing kiddos, and building cool things like this keeps me motivated (and sane!).  
If this has been useful to you, and you feel like saying thanks, you can **get me a beer or a coffee**—no pressure, just appreciation.  

[![Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/walksonair)

Cheers! 🍻

---

## 📜 License

This project is licensed under the **Apache License, Version 2.0**. See the [`LICENSE`](LICENSE) file for details.