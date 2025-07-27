## 1. Download the Setup Files

1. Click the green **`<> Code`** button at the top of this GitHub repo.
2. Select **Download ZIP**.
3. Unzip the downloaded file in your **Downloads** folder.

---

## 2. Set the Wallpaper

1. Locate the included wallpaper `.jpeg` file.
2. Right-click it and select **"Set as Wallpaper"**.

---

## 3. Enable Hidden Files

1. Open your **Files** (File Manager).
2. Click the **View** button and enable **Show Hidden Files**.

---

## 4. Install Icons and Cursors

1. Move the `Papirus` folders and the `volantes_light_cursors` folder to:
   ```
   /home/your-username/.icons
   ```

---

## 5. Install Themes

1. Move the `Adapta-Nokto` and `OrchideaDock` folders to:
   ```
   /home/your-username/.themes
   ```

---

## 6. Install Latte Dock

1. Open the terminal and run:
   ```bash
   sudo apt install latte-dock
   ```
2. Enter your password when prompted.
3. Type `y` and press Enter when asked for confirmation.
4. Once installed, run:
   ```bash
   latte-dock
   ```
5. A new dock should appear at the bottom of your screen.

---

## 7. Add Widgets to Latte Dock

1. Right-click the dock and choose **Add Widgets**.
2. Click the star icon to **Get New Widgets**.
3. Search and install the following:
   - `Mac OSX Inline Battery`
   - `Currently Playing` (choose the top result of the 3 ZIPs)
   - `Plasma Drawer`
   - `Latte Spacer`

---

## 8. Load Latte Layout

1. Right-click the dock and select **Configure Latte**.
2. Go to the **Layouts** tab.
3. Click **Import Layout**, and choose the layout file from the repo.
4. If successful, a top bar will appear.
5. You can now remove the original Cinnamon taskbar.

>  Some icons may be missing — don't worry, we’ll fix that below.

---

## 9. Apply Global Theme & Colors

1. Open the **Search Menu** and search for **Global Themes**.
2. Go to **Colors** or **Plasma Style**.
3. Import and apply the included **Midoriya** theme.

---

## 10. Fix Missing or Broken Icons

1. Run this in the terminal:
   ```bash
   sudo apt install papirus-icon-theme hicolor-icon-theme
   ```
2. This will fix most icon rendering issues.

> The terminal might still look odd — we’ll replace it later.

---

## 11. Add and Configure Clock Desklet

1. Right-click the desktop, choose **Add Desklets**.
2. Browse and download the **Timelet** desklet.
3. Go back to **Manage**, select **Timelet**, and click the **`+`** button to add it.
4. Right-click the clock to configure settings (e.g., set transparency to 100%).

> If the transparency looks blue, don’t worry — it’ll fix itself once you fully close all settings windows.

5. Drag the clock anywhere on your desktop.

---

## Done!

You now have a clean, modern, and customized Linux Mint desktop. If anything looks off or isn’t working, double-check the file paths and 
