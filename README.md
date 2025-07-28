# Make Linux Mint Beautiful (My Custom Setup)

This repo contains everything you need to transform your Linux Mint desktop into a cleaner, more modern look using Latte Dock, custom themes, icons, and widgets.

---

## Files Included

- Wallpaper image
- Custom Latte Dock layout
- Icon and cursor themes (`Papirus`, `volantes_light_cursors`)
- GTK and Plasma themes (`Adapta-Nokto`, `OrchideaDock`)

---

## How to Use

> **Note:** All steps below that are shown in gray code blocks should be run in the **Terminal**.
> You can open it by pressing `Ctrl + Alt + T` or by searching for "Terminal" in the start menu.
  

1. **Download the Setup Files**

    - Click the green **`<> Code`** button at the top of this repo
    - Select **Download ZIP**
    - Unzip the file in your **Downloads** folder

2. **Set the Wallpaper**

    - Right-click the wallpaper `.jpeg` and choose **"Set as Wallpaper"**

3. **Enable Hidden Files**

    - Open your file manager
    - Click the **View** button → enable **Show Hidden Files**

4. **Install Icons and Cursors**

```bash
mkdir -p ~/.icons
mv ~/Downloads/mint-beautiful-main/Papirus ~/.icons/
mv ~/Downloads/mint-beautiful-main/volantes_light_cursors ~/.icons/
```

5. **Install Themes**

```bash
mkdir -p ~/.themes
mv ~/Downloads/mint-beautiful-main/Adapta-Nokto ~/.themes/
mv ~/Downloads/mint-beautiful-main/OrchideaDock ~/.themes/
```

6. **Install Latte Dock**

```bash
sudo apt update
sudo apt install latte-dock
```

7. **Launch Latte Dock**

```bash
latte-dock
```

You should see a dock appear under your Cinnamon panel.

8. **Add Necessary Widgets**

> Some may already be installed by default, check you're widget menu if they're all there before continuing with step 9

- Right-click the Latte dock → **Add Widgets**
- Click the star icon to **Get New Widgets**
- Search and install the following (top ZIP if multiple options):
    - `Mac OSX Inline Battery`
    - `Digital Clock`
    - `Disk Usage`
    - `Memory Usage`
    - `Total CPU Use`
    - `Currently Playing`
    - `Bluetooth`
    - `System Tray`
    - `Lock/Logout`
    - `Plasma Drawer`
    - `Latte Spacer`
    - `SCP Menu`
    - `Search`
 
> If you can't find them they're probably already in your widget menu

9. **Load Custom Dock Layout**

- Right-click Latte dock → **Configure Latte**
- Go to **Layouts** tab → click **Import Layout**
- Choose the included layout file
- If successful, a top bar will appear — you can now remove the original Cinnamon taskbar

> There's a high chance that the folder icon on your bottom dock isnt rendering. The fix for this issue and other bugs encounter later in the process are shown under the "Fix Common Bugs" part

---
11. **Apply Global Theme**

- Open the Mint menu and search for **Global Themes**
- Go to **Plasma Style**
- Click Get New Plasma Styles and search for Midoriya, then install and apply it

## Add Clock Desklet

1. Right-click desktop → **Add Desklets**
2. Download and add the **Timelet** desklet
3. In **Manage**, click on it and press the **`+`** button to enable it
4. Right-click the clock to configure it (e.g., set transparency to 100%)

> If it appears blue, that will fix itself once you fully close all settings windows.

5. Drag the clock to your desired desktop location

---

## Fix Common Bugs

**Fix Missing Icons**

```bash
sudo apt install papirus-icon-theme hicolor-icon-theme
```
  
**Fix Logout and Lock Screen**

1. Right Click on SCP Menu on the bottom dock and click on "Configure SCP Menu"
2. Replace the command for "Lock Screen" with:
```bash
   cinnamon-screensaver-command -l
```
3. Replace the command for "Log Out" with:
```bash
  cinnamon-session-quit --logout --no-prompt
```
>This should fix the issue where the logout, and lock buttons weren't working.
>
>Personally, I use the Lock/Logout widget on the top dock. I wasn't able to fix it for that specific widget, but since I never use those buttons, I haven't bothered to dig further.
>
>If you'd like to remove that top widget, you can do so by editing the dock.
>    
>However, you might be able to fix it yourself by editing the widget's QML file. Go to:
>
>```bash
>/usr/share/plasma/plasmoids/org.kde.plasma.lock_logout/contents/ui/
>```

### **Partially Fixed: Right and Left Click Not Working for Stock Linux Mint Applications in Latte Dock**

This issue affects **stock Linux Mint applications** (like **Nemo** and **Firefox**) when one or more instances are running.

> **User-installed applications** (e.g., installed via `.deb`, `flatpak`, or manually) **do not have this issue**.

---

#### **Temporary Fix for Firefox**

You can restore click functionality for **Firefox** by:

1. **Removing** it via **Software Manager**
2. **Reinstalling** it again from Software Manager

---

#### **Other Stock Applications**

A similar approach *might* work for other stock apps, but this hasn't been fully tested yet.

---

### **Recommended Workaround**

Until a proper fix is available, use **screen edges** or **touchscreen gestures** to open or switch applications.

> To enable: open the **Start Menu** and search for them

---


## Done!

You now have a clean, modern Linux Mint desktop matching my personal setup.  
Enjoy your new look!
