# Make Linux Mint Beautiful

This repo contains everything you need to transform your Linux Mint desktop into a cleaner, more modern look using Latte Dock, custom themes, icons, and widgets.

---

## Files Included

- Wallpaper image (`Wallpaper.jpg`)
- Custom Latte Dock layout (`Used Dock.layout.latte`)
- Icon and cursor themes (`Papirus`, `volantes_light_cursors`)
- GTK and Plasma themes (`Adapta-Nokto`, `OrchideaDock`)
- My Fastfetch configuration file with custom modules and colors. (`config.jsonc`)
- Custom ASCII art displayed as the logo in terminal output. (`ascii.txt`)

---

## Important Notice

**Installing Latte Dock and mixing KDE components with the Cinnamon desktop environment can cause unexpected bugs, visual glitches, and instability.**

Users should always have a **backup of their system**.

If you're looking for a stable experience with this kind of look and feel, consider using a Linux distribution that uses **KDE Plasma by default**, such as:
 
 - **Kubuntu**
 - **Fedora KDE**
 - **Neon KDE**
 - **openSUSE KDE**
 
These are better suited for running Latte Dock and KDE widgets out of the box.

---

## Disclaimer

I'm very new to Linux, I've been using it for **about two weeks** and have **no prior experience with coding or scripting**.

Many of the solutions here were found through trial and error or searching online.
 
If you know better or more stable ways to solve any of the issues mentioned, **please open an issue or pull request** on this GitHub repository, your help would be really appreciated!

---

## How to Use

> **Note:** All steps below that are shown in gray code blocks should be run in the **Terminal**.
> You can open it by pressing `Ctrl + Alt + T` or by searching for "Terminal" in the start menu.
  

1. **Download the Setup Files**

    - Click the green **`<> Code`** button at the top of this repo
    - Select **Download ZIP**
    - Unzip the file in your **Downloads** folder
    - Also unzip the files inside the **cinnamon-latte-setup-main** folder

2. **Set the Wallpaper**

    - Right-click the wallpaper `.jpeg` and choose **"Set as Wallpaper"**

3. **Enable Hidden Files**

    - Open your file manager
    - Click the **View** button → enable **Show Hidden Files**

4. **Install Icons and Cursors**

```bash
mkdir -p ~/.icons
mv ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus ~/.icons/
mv ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus-Dark ~/.icons/
mv ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus-Light ~/.icons/
mv ~/Downloads/cinnamon-latte-setup-main/volantes_light_cursors ~/.icons/
```

5. **Install Themes**

```bash
mkdir -p ~/.themes
mv ~/Downloads/cinnamon-latte-setup-main/Adapta-Nokto ~/.themes/
mv ~/Downloads/cinnamon-latte-setup-main/Orchidea ~/.themes/
```

6. **Select Theme in Settings**
- Click on the Mint homebutton
- Type **Themes** in the searchbar and open it
- Click on the `Advanced Settings` button
- Select volantes_light_cursor for Mouse Pointer
- Select Adapta-Nokto for Applications
- Select Papirus for Icons
- Select Orchidea for Desktop

  
7. **Install Latte Dock**

```bash
sudo apt update
sudo apt install latte-dock
```

8. **Launch Latte Dock**

```bash
latte-dock
```

You should see a dock appear under your Cinnamon panel.

9. **Add Necessary Widgets**

> Some may already be installed by default, check your widget menu if they're all there before continuing with Step 9.

- Right-click the Latte dock and click on `Add Widgets`
- Click the star icon to `Get New Widgets`
- Search and install the following (top ZIP if multiple options):
    - `Big Sur - Inline Battery`
    - `Currently Playing`
    - `Plasma Drawer`
    - `Latte Spacer`
    - `Simple Customizable Power Menu`

10. **Load Custom Dock Layout**

- Right-click Latte dock, and click on `Configure Latte`
- Go to **Layouts** tab, and click on `Import Layout`
- Choose the included layout file and press `Apply`
- Now select `Used Dock` and press on `Switch`
- If successful, a top and bottom bar will appear.
- You can now remove the original Cinnamon taskbar by right-clicking on it and select `remove`

> The Top and Bottom bar will probably be hiding. If you want to change that, hover around the top or bottom part of the screen, right click the dock, and select `Edit Dock`. You can now change the visibility settings and other settings if you want. You will need to do this individually for each dock.

> There's a high chance that the folder icon on your bottom dock isnt rendering. The fix for this issue and other bugs encounter later in the process are shown under the "Fix Common Bugs" part

11. **Fix Widgets**

Some of the top Widgets will probably not be working so here's how to fix that:

**If the Battery Widget is displaced:**
- Right-click on the top dock and press `Edit Dock`
- Drag the Inline Battery to the top left

**If the Digital Clock is the wrong size:**
- Right-click on the Digital Clock dock and press `Configure Digital Clock`
- Scroll down and click on `Choose Style`
- Choose your preferred text size

**If the System Monitoring widgets are not shown / not shown correctly:**
- Add the `Disk Usage` widget to the top bar and select `Configure Disk Usage`
- Select `Get New Display Styles`, and Install `Colored Text` by gernperl
- Restart Latte-Dock:
```bash
killall latte-dock && latte-dock &
```
---
11. **Apply Global Theme**

- Open the Mint menu and search for **Global Themes**
- Go to **Plasma Style**
- Click `Get New Plasma Styles` and search for `Midoriya`, then install and apply it

## Add Clock Desklet

1. Right-click desktop and click on `Add Desklets`
2. Download and add the `Timelet` desklet
3. In `Manage`, click on it and press the **`+`** button to enable it
4. Right-click the clock to configure it (e.g., set transparency to 100%)

> If it appears blue, that will fix itself once you fully close all settings windows.

5. Drag the clock to your desired desktop location

---

## Login Window

To match your login screen with your desktop setup, do the following:

1. **Open the Start Menu** and search for **Login Window**
2. Go to the **Appearance** tab
3. Under **Background**, click the image preview  
   → Select the included `wallpaper.jpg` from your Downloads folder
4. Scroll down to **Icon Theme**  
   → Select `Papirus`  
5. Scroll further down to **Mouse Cursor**  
   → Select `volantes_light_cursors` 
6. Click **Apply** to save changes

> **Log out or reboot** to see the updated login screen.

---

# Fastfetch Config + Custom ASCII Logo

1. **Install Kitty Terminal** 

```bash
sudo apt update  
sudo apt install kitty
```

2. **Set Kitty Terminal as default** 

```bash
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator ~/.local/kitty.app/bin/kitty 50
sudo update-alternatives --config x-terminal-emulator
```
3. **Choose Kitty from the list, and type in the correct number**
    
4. **Close your Terminal and use Ctrl + Alt + T. Check if you're using the Kitty Terminal, and use that Terminal for all the following steps**

5. **Install fastfetch**

```bash
sudo apt update  
sudo apt install fastfetch   
```

6. **Create the Fastfetch config folder** (if it doesn’t exist):

```bash
mkdir -p ~/.config/fastfetch
```

7. **Copy the files into your config directory** 

```bash
cp ~/Downloads/cinnamon-latte-setup-main/config.jsonc ~/.config/fastfetch/config.jsonc
cp ~/Downloads/cinnamon-latte-setup-main/ascii.txt ~/.config/fastfetch/ascii.txt
```

8. **Run Fastfetch** 

```bash
fastfetch
```
## Fastfetch ASCII Art Customization

To replace the logo with your own custom ASCII art:

1. **Open the ASCII logo file in a text editor**

```bash
xed ~/.config/fastfetch/ascii.txt
```

2. **Replace the existing art with your own, then save and close the file**

3. **Run Fastfetch again to see your changes**

```bash
fastfetch
```

## Fastfetch Color Customization

In your config.jsonc, you can set colors using ANSI codes or 24-bit RGB values.  

To open the config.jsonc file:

```bash
xed ~/.config/fastfetch/config.jsonc
```

**Examples of color codes:**

31 = red  
32 = green  
34 = blue  

RGB format: 38;2;&lt;R&gt;;&lt;G&gt;;&lt;B&gt;    
Example: ```38;2;152;255;152 ``` for pastel green  

**To apply the color, change the relevant color key in your config.jsonc, for example:**

```bash
"keyColor": "38;2;152;255;152"
```
or
```bash
"keyColor": "32"  
```
**Note on Line Breaks**

You can remove the line breaks ("break") in the config file if you want. I put them there so you can't see my username, and the hostname at the command line. The same applies to the spaces in the ascii.txt file.

## Terminal transparency:

Use the following code in kitty and choose a value between 0.0 and 1.0 (I used 0.8 on my pc).

0.0 = fully transparent  
1.0 = fully opaque  

```bash
echo "background_opacity 0.8" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty
```

## Terminal color:

Use the following code in kitty and use a Hex code for the color you want to use (in the code example the hex code = #28353b, which is a dark-cyan-gray color).

```bash
echo "background #28353b" >> ~/.config/kitty/kitty.conf && killall -SIGUSR1 kitty
```

---

## Fix Common Bugs

**Fix Missing Icons:**

```bash
sudo apt install papirus-icon-theme hicolor-icon-theme
```
---

**Fix Logout and Lock Screen:**

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
---

**Partially Fixed: Right and Left Click Not Working for Stock Linux Mint Applications in Latte Dock**

This issue affects **stock Linux Mint applications** (like **Nemo** and **Firefox**) when one or more instances are running.

> **User-installed applications** (e.g., installed via `.deb`, `flatpak`, or manually) **do not have this issue**.
  
You can restore click functionality for **Firefox** by:
  
1. **Removing** it via **Software Manager**
2. **Reinstalling** it again from Software Manager
  
A similar approach might work for other stock apps, but I haven't tested this.
  
**Recommended Workaround**

Until a proper fix is available, use **screen edges** or **touchscreen gestures** to open or switch applications.

> To enable: open the **Start Menu** and search for them

---


## Done!

You now have a clean, modern Linux Mint desktop matching my personal setup.  
Enjoy the new look!

If you have any questions or issues, I'm happy to help!
