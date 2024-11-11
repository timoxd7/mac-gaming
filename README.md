# Mac Gaming

This is my own small collection of information to get my games and launchers working and not to forget how i did it. Maybe someone will benefit from it too.

## Whisky Setup

Whisky works simple, but some games only work with a version previous to WhiskyWine (the wine fork from Whisky team). For me, Whisky 2.2.4 worked best. The setup of the newest Whisky version is just download it, but to use the older version, you need this guide: [Whisky v2.2.4 Usage](Whisky.md)

Games tested and worked:
- Planet Coaster (1)

To use Steam at the current state, see [this comment](https://github.com/Whisky-App/Whisky/issues/1199#issuecomment-2460454741).


## GPTK Setup

GPTK is a more bare-metal approach, installing in a terminal. See [WinSteamOnMac](https://github.com/domschl/WinSteamOnMac) how to set up homebrew and gptk for x86 on your mac. After that, see [GPTK](GPTK.md) for more information.

To use Steam at the current state, see [this comment](https://github.com/Whisky-App/Whisky/issues/1199#issuecomment-2460454741).


## Steam

To use Steam at the current state, see [this comment](https://github.com/Whisky-App/Whisky/issues/1199#issuecomment-2460454741).

For [Whisky](Whisky.md), add these as additional starting arguments. For [GPTK](GPTK.md), use the arguments postponed to your ...steam.exe call.

## Ubisoft Connect

See [this](https://github.com/Whisky-App/Whisky/issues/273#issuecomment-2166537483) for more information. Currently you need to install dotnet48 to get Ubisoft Connect working. Install it with winetricks either with the command line OR using the GUI. If using the GPTK Setup, you need the following command as no GUI is there:

    winetricks -q dotnet48

Then remove the cache folder `drive_c/Program Files (x86)/Ubisoft/Ubisoft Game Launcher/cache` to get it working again.
