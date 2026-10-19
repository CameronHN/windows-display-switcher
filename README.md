# Windows Display Switcher

A set of Windows batch file scripts that will change your display settings.

## NOTE

These scripts are intended for dual display setups and will only work on Windows 10 and 11 systems.

## Purpose

These scripts change your display settings without you having to go to your settings to change them. Use the single menu script (`DisplayMenu.bat`) to pick a mode with one keypress, or use one of the individual scripts for a direct one-action shortcut.

### Prerequisites

Understand the following before running a script:

* Understand the layout of your dual display setup.
* Head to your settings and identify your displays.
* Each display will be identified with a number. Take note of these numbers.

![GIF on how to identify displays](assets/videos/Untitledvideo3-ezgif.com-video-to-gif-converter.gif)

### Installation

To execute a script, simply double click on the file.

## Usage

![GIF selecting display type](assets/videos/SelectDisplayType.gif)

### Menu script

Not sure which script you need? Double click `DisplayMenu.bat` and press a single key (no Enter required):

| Key | Action |
|-----|--------|
| `e` | Extend the displays |
| `d` | Duplicate the displays |
| `1` | Show only on display 1 |
| `2` | Show only on display 2 |

Any other key is ignored and the menu keeps waiting for a valid one. The script exits as soon as a mode is applied.

#### Launch the menu at login

You can set `DisplayMenu.bat` up to run automatically when you log in to your account using the Windows Task Scheduler. This lets you pick the display setting you want from the moment you log in.

1. Open **Task Scheduler** from the Start menu.
2. Select **Create Task...** in the right-hand Actions pane.
3. On the **General** tab, give the task a name (for example, `Display Menu`).
4. On the **Triggers** tab, select **New...**, set **Begin the task** to **At log on**, choose **Specific user** and select your account, then select **OK**.
5. On the **Actions** tab, select **New...**, leave the action as **Start a program**, browse to `DisplayMenu.bat`, then select **OK**.
6. Select **OK** to save the task.

The menu will now appear each time you log in.

### Individual scripts

If you want a direct one-action shortcut, use one of the individual scripts:

1. InternalDisplay.bat
   - Display only on display 1
   - Performs 'Show only on 1'
2. ExternalDisplay.bat
   - Display only on display 2
   - Performs 'Show only on 2'
3. DuplicateDisplays.bat
   - Clone/Duplicate the displays
   - Performs 'Duplicate these displays'
4. ExtendDisplays.bat
   - Extend the displays
   - Performs 'Extend these displays'
