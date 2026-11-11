# Trading Desk for Windows

The Windows installer for **Trading Desk**, a local decision-support desk for stocks and crypto by [FutureInvoked](https://futureinvoked.uk/projects/trading-desk/). It runs on your PC, reads free market data, checks your own rules and never places orders.

**Download:** [the latest release](https://github.com/FutureInvoked/trading-desk-windows/releases/latest) → `TradingDesk-Setup-<version>.exe`. The project page, the first-run guide and the source zip for Mac and Linux are on [futureinvoked.uk](https://futureinvoked.uk/projects/trading-desk/#download).

## What the installer does

- Installs for your Windows user only, without administrator rights and without needing the internet while it installs.
- Brings its own Python 3.12 and every package the desk uses, checked against their SHA-256 hashes.
- Puts the app in `%LOCALAPPDATA%\Programs\Trading Desk` and the desk, its Python and your data in `%LOCALAPPDATA%\TradingDesk`.
- Adds Trading Desk to the Start menu and to Settings > Apps, where you can uninstall it. Uninstalling asks whether to delete your portfolio and data too.
- Installing a newer version keeps your portfolio, the desk's data and your edited `config\desk.toml`.
- It opens with a fictional demo portfolio, so every page has something to show.

Tested on Windows 11. The window uses Microsoft Edge WebView2, which Windows 11 already has.

## "Windows protected your PC"

The installer isn't code-signed yet, so Microsoft Defender SmartScreen may say the publisher is unknown. Choose **More info**, then **Run anyway**. Check the file first: its SHA-256 is in the release notes and on the project page.

```powershell
Get-FileHash .\TradingDesk-Setup-0.2.0.exe -Algorithm SHA256
```

## Licence

Trading Desk is source-available for personal use, not open source: see [LICENSE](LICENSE). The installer also carries CPython (Python Software Foundation License), the Python packages the desk depends on (each under its own licence, which is installed with it) and Microsoft's WebView2 SDK files (licence and notice beside the app).

Decision support only: not financial, investment, tax or legal advice.

Questions: futureinvoked@proton.me
