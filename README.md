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

- Right-click the Latte dock → **Add Widgets**
- Click the star icon to **Get New Widgets**
- Search and install the following:
    - `Mac OSX Inline Battery`
    - `Currently Playing` (top ZIP if multiple options)
    - `Plasma Drawer`
    - `Latte Spacer`

9. **Load Custom Dock Layout**

- Right-click Latte dock → **Configure Latte**
- Go to **Layouts** tab → click **Import Layout**
- Choose the included layout file
- If successful, a top bar will appear — you can now remove the original Cinnamon taskbar

> If some icons are missing, continue to the next step.

10. **Fix Missing Icons**

```bash
sudo apt install papirus-icon-theme hicolor-icon-theme
```

> This resolves the folder icon issue.

---
11. **Apply Global Theme**

- Open the Mint menu and search for **Global Themes**
- Go to **Colors** or **Plasma Style**
- Import and apply the **Midoriya** theme included in the repo


## Add Clock Desklet

1. Right-click desktop → **Add Desklets**
2. Download and add the **Timelet** desklet
3. In **Manage**, click on it and press the **`+`** button to enable it
4. Right-click the clock to configure it (e.g., set transparency to 100%)

> If it appears blue, that will fix itself once you fully close all settings windows.

5. Drag the clock to your desired desktop location

---

## Done!

You now have a clean, modern Linux Mint desktop matching my personal setup.  
Enjoy your new look!
