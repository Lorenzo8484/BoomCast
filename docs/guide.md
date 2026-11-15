# BoomCast user guide

*Italiano: [guida.it.md](guida.it.md)*

## Before you start

1. The PC and the speaker must be on the same home network.
2. In Apple's **Home** app open *Home Settings → Speakers & TVs* and under *Allow Speaker & TV Access* choose **Anyone on the Same Network**. Without this the speaker refuses the connection.
3. Run `BoomCast.exe`. If Windows shows "Windows protected your PC", choose *More info → Run anyway*: this appears because the file is not digitally signed.

## Speakers

Every speaker found on the network has its own card.

- **Switch at the top right:** starts or stops streaming to that speaker.
- **Volume:** for that speaker only. The *Master volume* in the left column scales all of them together.
- **Extra delay:** adds delay to that speaker alone, to line it up with others or with a video.
- **Auto-reconnect:** if a phone takes the speaker, BoomCast steps aside and comes back by itself when the phone is done. It also applies when the connection drops. Off: it stays disconnected until you switch it on again.
- **Reconnect wait:** how many seconds without audio from the phone must pass before BoomCast streams again (5 seconds to 5 minutes, 30 by default). While it waits, a countdown shows next to the speaker's name.

At the top, **Stop all** disconnects every speaker.

## Sound

- **"Audio enhancements" switch:** off, the sound passes through unchanged.
- **Modes:** nine built in (Flat, Bass+, Voice, Movie, Music, Night, Game, Spatial, Concert) plus your own. *Flat* is the normal sound, with everything at zero.
- **Every mode remembers your adjustments.** If you move a slider while a mode is on, the change belongs to that mode, even after a restart; an orange dot marks the modes you have changed. **Reset** puts the active mode back to its base settings and leaves the others alone.
- **Save sound settings…** stores everything on the page under a name of your choice. It always creates a new mode; if the name exists, a number is added. The × on one of your modes deletes it.
- **Reordering:** hold a mode and drag it where you want.
- **Equaliser:** ten bands from 31 Hz to 16 kHz, plus the preamp (*Pre*). Lower *Pre* when you raise bands a lot, to avoid distortion. Double-click a slider to put it back to neutral.
- **Spatial sound:** stereo width, surround, reverb, room size, channel blend, balance.
- **Dynamics:** compression, even volume, limiter, dithering.

The bars at the top show the level per band; beside the equaliser are left channel, centre, sides and right channel.

## Settings

- **Startup:** start with Windows, close to the notification area (the X hides the window and the sound goes on), language. *Auto* uses the language of Windows, or English when it is not available.
- **Audio to stream:** the Windows output to capture. *Default* follows the one you pick in Windows.
- **Delay:** how long the speaker waits before playing. Lower is more responsive; higher copes better with weak Wi-Fi.
- **Streaming:**
  - *HomePod only* mutes the PC speakers while streaming.
  - *ALAC compression* makes packets smaller without losing quality and reduces dropouts on Wi-Fi. Off, uncompressed PCM is used.
  - *PC buffer* is a small reserve of audio on the PC: raise it if the log shows "buchi" (dropouts).
- **Firewall:** state of the permission and a button to grant it.
- **Add by IP address:** for speakers the automatic search does not find.
- **Log:** what the app has done, useful to understand a problem. It is written in Italian.

## Notification area

The icon stays next to the clock. Left click: opens the window. Right click: opens a panel with the speakers (switch and volume), the settings and the exit.

## Common problems

| What happens | What to do |
|---|---|
| No speaker found | Check that the PC and the speaker are on the same network and that in the Home app access is set to "Anyone on the Same Network". On networks with several access points or with device isolation the search can fail: use *Add by IP address*. |
| "Blocked by Windows Firewall" | Press *Allow in firewall* and confirm the Windows prompt. If you moved or renamed the file, the permission must be given again. |
| The connection is refused | Almost always the access setting in the Home app. A speaker protected by a password or code is not supported. |
| The sound stutters | Keep ALAC compression on and raise the delay (*Video* or *Music*). The dropouts come from the speaker's Wi-Fi: moving it closer to the router or using a quieter channel helps. |
| Audio is late compared with the video | Lower the delay, or delay the video in your player by the same amount. |
| After the iPhone, the PC sound does not come back | Check that *Auto-reconnect* is on for that speaker and watch the countdown. It starts only when the phone no longer sends audio. |
| Distorted sound | Lower *Pre* in the equaliser and keep the limiter on. |

If that does not solve it, open an issue in the **Issues** section and attach the text of the Log.

## Where the data is

Settings and the log are in `%APPDATA%\BoomCast`. To start from scratch, close BoomCast and delete that folder. To remove BoomCast, delete `BoomCast.exe` and, if you like, that folder.
