# My Karabiner Configuration

This repository contains my custom Karabiner-Elements configuration for efficient app switching and keyboard shortcuts on macOS.

## Features

### Dynamic App Slot System
- **Alt + Shift + `** → Set current app as main slot
- **Alt + `** or **Caps Lock alone** → Open app in main slot
- Shows notification when setting the main app slot

### Direct App Shortcuts (Numbers)
- **Alt + 1** → Visual Studio Code
- **Alt + 2** → iTerm
- **Alt + 3** → Sequel Ace
- **Alt + 4** → Sublime Text

### Direct App Shortcuts (Letters)
- **Alt + Q** → Arc Browser
- **Alt + W** → Firefox
- **Alt + E** → Notion
- **Alt + F** → Finder
- **Alt + A** → Discord
- **Alt + S** → Messenger
- **Alt + D** → WhatsApp
- **Alt + Z** → Spotify
- **Alt + X** → YouTube Music
- **Alt + C** → Zen Browser

### System Navigation
- **Cmd alone** → Switch to most recent app (Cmd+Tab)
- **Control alone** → Cycle through windows of same app (Cmd+`)

## Installation

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
2. Copy `karabiner.json` to `~/.config/karabiner/karabiner.json`
3. Restart Karabiner-Elements or reload the configuration

## Usage

### Setting Up Your Main App Slot
1. Open the app you want to set as your main slot
2. Press **Alt + Shift + `** to set it
3. You'll see a notification confirming the app was set
4. Now you can quickly switch to this app using **Alt + `** or **Caps Lock alone**

### Left-Hand Optimized Design
All shortcuts are designed to be used with the left hand only, making it easy to switch apps while using a mouse or trackpad with your right hand.

## Customization

To modify app shortcuts:
1. Edit `karabiner.json`
2. Change the `shell_command` value to `open -a 'Your App Name'`
3. Restart Karabiner-Elements to apply changes

## Technical Details

- Uses shell commands with `open -a` for app launching
- Dynamic slot system stores the current app in `/tmp/karabiner_main_app`
- AppleScript integration for notifications and app detection
- Compatible with macOS keyboard shortcuts and system behavior

## Troubleshooting

- **App not opening**: Check that the app name in the configuration matches the exact name in `/Applications`
- **Shortcuts not working**: Restart Karabiner-Elements or check that it has the necessary permissions
- **VS Code detection issues**: The configuration handles both "Code" and "Visual Studio Code" process names

## File Structure

```
├── karabiner.json          # Main configuration file
├── README.md              # This file
├── assets/
│   └── complex_modifications/
└── automatic_backups/
    └── karabiner_*.json   # Automatic backups
```
