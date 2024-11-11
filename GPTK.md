# GPTK Terminal Setup

First see [WinSteamOnMac](https://github.com/domschl/WinSteamOnMac) how to install wine and GPTK easily on your system. This here are only additional infos.

On Terminal, you can define so called environment variables by setting them in front of the actual command. The following variables are recommended with newest GPTK:

    MTL_HUD_ENABLED=0
    WINEESYNC=1
    ROSETTA_ADVERTISE_AVX=1

For example, running Steam, you call (See [README](README.md) for more infos for current Steam)

    MTL_HUD_ENABLED=0 WINEESYNC=1 ROSETTA_ADVERTISE_AVX=1 /Applications/Game\ Porting\ Toolkit.app/Contents/Resources/wine/bin/wine ~/.wine/drive_c/Program\ Files\ \(x86\)/Steam/steam.exe

Note that the Filesystem is not in a virtual HDD or so, it is your root file system. You can have multiple wine prefix, which is kind of a configuration, plus a filesystem that should be used for this "virtual" windows. However, this windows is not virtual, it is just translating sys-calls, so runs almost in native performance (wine stands for wine is not an emulator, get it apple). To set your wine prefix (so the folder which should be used as root for the pretended windows system), use

    WINEPREFIX=/here/your/path

## Running programs

Use

    MTL_HUD_ENABLED=0 WINEESYNC=1 ROSETTA_ADVERTISE_AVX=1 /Applications/Game\ Porting\ Toolkit.app/Contents/Resources/wine/bin/wine /your/program.exe

to start a program. Either prepend your WINEPREFIX (if not uses default ~/.wine one) or set it previously as environment variable using `export WINEPREFIX=~/.wine`.

## winecfg

You can configure Wine with wineconfig using

    MTL_HUD_ENABLED=0 WINEESYNC=1 ROSETTA_ADVERTISE_AVX=1 /Applications/Game\ Porting\ Toolkit.app/Contents/Resources/wine/bin/wine winecfg

You can set e.g. the Windows Version and more there.

## winetricks

This is a small tool to manage some default tasks. Just install it using your x86 brew and run it while setting wineprefix before (if not using default one).
