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

If you're looking for a stable experience with this kind of look and feel, consider using a Linux distribution that uses **KDE Plasma by default**, such as but not limited to:
 
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
    - Unzip the file in your **Downloads** folder by clicking on `Extract Here`
    - Also unzip the files inside the **cinnamon-latte-setup-main** folder with `Extract Here`

2. **Set the Wallpaper**

    - Right-click the wallpaper `.jpeg` and choose **"Set as Wallpaper"**

3. **Enable Hidden Files**

    - Open your file manager
    - Click the **View** button → enable **Show Hidden Files**

4. **Moving Everything to the right directory**

```bash
cp -r ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus ~/.icons/
cp -r ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus-Dark ~/.icons/
cp -r ~/Downloads/cinnamon-latte-setup-main/papirus-icon-theme-yellow-folders/Papirus-Light ~/.icons/
cp -r ~/Downloads/cinnamon-latte-setup-main/volantes_light_cursors ~/.icons/
cp -r ~/Downloads/cinnamon-latte-setup-main/Adapta-Nokto ~/.themes/
cp -r ~/Downloads/cinnamon-latte-setup-main/Orchidea ~/.themes/
sudo cp -r ~/Downloads/cinnamon-latte-setup-main/volantes_light_cursors /usr/share/icons/
sudo cp ~/Downloads/cinnamon-latte-setup-main/Wallpaper.jpg /usr/share/backgrounds/linuxmint/
```

5. **Select Theme in Settings**
- Click on the Mint homebutton
- Type **Themes** in the searchbar and open it
- Click on the `Advanced Settings` button
- Select `volantes_light_cursor` for Mouse Pointer
- Select `Adapta-Nokto` for Applications
- Select `Papirus` for Icons
- Select `Orchidea` for Desktop

  
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

- Right-click the Latte dock and click on `Add Widgets`
- Click the star icon to `Get New Widgets`
- Search and install the following (top ZIP if multiple options):
    - `Big Sur - Inline Battery`
    - `Currently Playing`
    - `Plasma Drawer`
    - `Latte Spacer`
    - `Simple Customizable Power Menu`
 
 > Check your widget menu if they're all there before continuing with Step 9.

9. **Load Custom Dock Layout**

- Right-click Latte dock, and click on `Configure Latte`
- Go to **Layouts Editor** tab, and click on `Import Layout`
- Choose the included layout file `Used Dock.layout.latte` in the **cinnamon-latte-setup-main folder** and press `Apply`
- Now select `Used Dock` and press on `Switch`
- If successful, a top and bottom bar will appear. (They might not be visible if you have a window maximized)
- You can now remove the original Cinnamon taskbar by right-clicking on it and select `remove`

> The Top and Bottom bar are set to dodge all windows. If you want to change that, hover around the top or bottom part of the screen (if they're not visible), right click the dock, and select `Edit Dock`. You can now change the visibility settings and other settings if you want. You will need to do this individually for each dock.

> There's a chance that the folder icon on your bottom dock isn't rendering. The fix for this issue, and other bugs encounter later in the process, are shown under the "Fix Common Bugs" part at the bottom of the README.md

10. **Fix Widgets**

Some of the top Widgets will probably not be working, so here's how to fix that:

**If the Battery Widget is displaced:**
- Right-click on the top dock and press `Edit Dock`
- Drag the Inline Battery to the top left

**If the Digital Clock is the wrong size:**
- Right-click on the Digital Clock dock and press `Configure Digital Clock`
- Scroll down and click on `Choose Style`
- Choose your preferred text size

**If the System Monitoring widgets are not shown / not shown correctly:**
- Add the `Disk Usage` widget to the top bar and select `Configure Disk Usage` by right-clicking on it in the dock.
- Select `Get New Display Styles`, and install `Colored Text` by gernperl
- Restart Latte-Dock:
```bash
killall latte-dock && latte-dock &
```
- If the `Disk Usage` widget that you added is still on the dock, you can delete it by right-clicking on the dock, click on `Edit Dock`, and hover over the widget you want to remove.
  
---
11. **Apply Global Theme**

- Open the KDE menu (lower left) and search for **Global Themes**
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
2. If asked for `Run as root` click on `Ignore` and continue
3. Go to the **Appearance** tab
4. Under **Background**, click the image preview  
   → Select the `wallpaper.jpg` in the currently opened folder
5. Scroll down to **Icon Theme**  
   → Select `Papirus`  
6. Scroll further down to **Mouse Cursor**  
   → Select `volantes_light_cursors` 
7. Click **Apply** to save changes
8. **Reboot** to see the updated login screen.
   
> Log out will probably not work, the fix can be found under `Fix Common Bugs` at the bottom of the README.md

---

# Fastfetch Config + Custom ASCII Logo

1. Install Kitty Terminal

```bash
sudo apt update  
sudo apt install kitty
```

2. Set Kitty Terminal as default

```bash
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator ~/.local/kitty.app/bin/kitty 50
sudo update-alternatives --config x-terminal-emulator
```
3. Choose Kitty from the list, and type in the correct number
    
4. Close your Terminal with:
```bash
pkill gnome-terminal
```
6. Ctrl + Alt + T. Check if you're using the Kitty Terminal, and use that Terminal for all the following steps**
> If the default Terminal doesn't change: go to `Preferred Applications` by typing it in the menu search bar. Scroll all the way down, and change terminal to kitty

7. Install Fastfetch

```bash
sudo add-apt-repository ppa:zhangsongcui3371/fastfetch
sudo apt update  
sudo apt install fastfetch   
```

8. Install Nerd Font for Icons

```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts
wget https://github.com/ryanoasis/nerd-fonts/releases/latest/download/Meslo.zip
unzip Meslo.zip
fc-cache -fv
```

9. Create the Fastfetch config folder (if it doesn’t exist):

```bash
mkdir -p ~/.config/fastfetch
```

10. Copy the files into your config directory

```bash
cp ~/Downloads/cinnamon-latte-setup-main/config.jsonc ~/.config/fastfetch/config.jsonc
cp ~/Downloads/cinnamon-latte-setup-main/ascii.txt ~/.config/fastfetch/ascii.txt
```

12. Run Fastfetch

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

> For more customization you can also install Fastcat: https://github.com/m3tozz/FastCat
>
> ```bash
> git clone --depth 1 https://github.com/m3tozz/FastCat.git && cd FastCat && bash ./fastcat.sh --shell
> ```

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
> You might need to restart Kitty for the opacity setting to take effect
  
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
> You might need to check the boxes that remain unticked on the left column to find Lock Screen & Logout

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
2. **Unpin** from the Dock
3. **Reinstalling** it again from Software Manager (If System Package doesn't work, try Flatpak)
  
A similar approach might work for other stock apps, but I haven't tested this.
  
**Recommended Workaround**

Until a proper fix is available, use **Hot Corners** or **Gestures** to open or switch applications.

> To enable: open the **Start Menu** and search for them

---


## Done!

You now have a clean, modern Linux Mint desktop matching my personal setup.  
Enjoy the new look!

If you have any questions or issues, I'm happy to help!
