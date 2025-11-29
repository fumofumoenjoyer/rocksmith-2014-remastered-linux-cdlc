# rocksmith-2014-remastered-linux-cdlc
tutorial for rocksmith 2014 remastered for linux with cdlc support, this is from

https://customsforge.com/topic/67471-cdlc-on-linux-instructions/

## Get the cable working:

Pre-requirements
Install Rocksmith 2014
Install wine, winetricks
Before anything next, plug in the Rocksmith Real Tone Cable to the USB port. Once done, execute below commands in your terminal. By default game is installed in /home/user/.steam/steam and this path will be used in all examples.

Wine configuration
Execute below lines:
```
WINEPREFIX=~/.steam/steam/steamapps/compatdata/221680/pfx winetricks sound=alsa
WINEPREFIX=~/.steam/steam/steamapps/compatdata/221680/pfx winecfg
```
Change below options in "window" that appeared:

```
Applications tab:
    Windows Version: Windows 10
Drives tab:
    Drive Z: /home/user/.steam/steam (default, might be other)
Audio tab:
    Input device: In: Rocksmith USB Guitar Adapter
    Voice input device: In: Rocksmith USB Guitar Adapter
```
Apply changes by clicking ok button.

Steam configuration
It's time to launch the game for the first time. Go to properties of the game on steam and change LAUNCH OPTIONS, as below:
```
PROTON_NO_D3D11=1 %command%
```
Now launch the game. This step is only required in order to create Rocksmith.ini file in ```~/.steam/steam/steamapps/common/Rocksmith2014.```

Game configuration
Open Rocksmith.ini and change two parameters:
```
ExclusiveMode=0
Win32UltraLowLatencyMode=0
```
That's it. Launch the game. You are ready to calibrate your guitar and start playing some cool stuff.

Sound configuration
It's worth to check the volume of your guitar. Please go to the sound settings in OS and tune the volume of your guitar in input/mics section. 100% is fine.
