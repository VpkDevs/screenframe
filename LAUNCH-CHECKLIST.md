# Windows Margin Manager Launch Checklist

## Offer

- Listing: Gumroad.
- Price test: $9 one-time for the first 25 buyers, then $19.
- Buyer: Windows users with ultrawide or multi-monitor setups who repeatedly resize the same application windows.
- Pitch: apply reusable breathing room and layouts to your Windows desktop from the system tray.

## Before Publishing

```powershell
dotnet build -c Release
dotnet publish -c Release -r win-x64 --self-contained true
```

- Run the published executable on Windows 10 and Windows 11.
- Verify apply, restore, tile, profile switching, tray exit, and monitor reconnect behavior.
- Add a real application icon before the first public ZIP.
- Capture a short before-and-after screen recording.

## Delivery Boundary

- Sell only the tray utility that exists today.
- Do not advertise a CLI, REST API, service mode, or plugin system yet.
- Treat the manual checklist in `TESTING.md` as required release work.
