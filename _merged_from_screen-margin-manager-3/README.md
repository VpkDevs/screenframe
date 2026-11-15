# Windows Margin Manager

Windows Margin Manager is a Windows tray utility for applying reusable margins and layouts to desktop windows. It is aimed at people who want a little breathing room around application windows without manually resizing them all day.

## Current Capabilities

- Apply and restore desktop window margins from the tray.
- Save named profiles and switch between them with hotkeys.
- Tile or distribute windows across monitors.
- Configure per-monitor margins.
- Schedule profile and margin actions.
- Apply basic adaptive positioning and animation settings.

## Build

Requirements:

- Windows 10 or Windows 11.
- .NET 8 SDK.

```powershell
dotnet restore
dotnet build -c Release
```

## Run

```powershell
dotnet run
```

The application starts in the Windows system tray. Right-click the tray icon to configure margins, profiles, monitors, and scheduled actions.

## Publish A Standalone Build

```powershell
dotnet publish -c Release -r win-x64 --self-contained true
```

The publish output is written below `bin\Release\net8.0-windows\win-x64\publish\`.

## Core Hotkeys

| Hotkey | Action |
|---|---|
| `Ctrl+Alt+M` | Apply or restore margins |
| `Ctrl+Alt+R` | Restore original positions |
| `Ctrl+Alt+A` | Auto-arrange windows |
| `Ctrl+Alt+T` | Tile windows |
| `Ctrl+Alt+S` | Save the current layout |
| `Ctrl+Alt+1-9` | Switch profiles |
| `Win+Shift+M` | Distribute windows across monitors |

## Shipping Notes

This is a Windows-only desktop utility. Before selling a build, manually verify tray startup, hotkey registration, restore behavior, and multi-monitor layouts on the Windows versions you plan to support. See `TESTING.md` for the full checklist.

The project does not currently expose a CLI, REST API, plugin system, or Windows service mode. Those are possible future features, not shipped capabilities.
