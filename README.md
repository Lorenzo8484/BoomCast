# BoomCast

**Play everything your Windows PC plays on your HomePod.** BoomCast sends the PC's sound to HomePod and other AirPlay 2 speakers over your home network. No driver to install, no account, free.

*Italiano: [README.it.md](README.it.md)*

> BoomCast is an independent project. It is not affiliated with, endorsed by or approved by Apple. AirPlay, HomePod, HomeKit and iPhone are trademarks of Apple Inc.

## What it does

- **PC sound on the speaker.** Whatever plays on the chosen Windows output (music, video, games, calls) goes to the speakers you switch on. Several speakers can play together.
- **Low delay.** Four delay presets, from *Instant* (0.15 s) for games and video to *Music* (0.9 s) for weak Wi-Fi, plus a free slider.
- **Lossless.** 44.1 kHz / 16 bit, sent as ALAC (smaller packets, fewer dropouts on Wi-Fi) or uncompressed PCM.
- **Sound shaping.** 10-band equaliser, bass, brightness, voice, stereo width, surround, reverb, compressor, limiter. Nine built-in sound modes; every mode remembers your own adjustments, and you can save your own under any name and drag them into the order you like.
- **Live meters.** Spectrum by band, left/right, centre and sides.
- **Shares the speaker with your phone.** When an iPhone starts playing on the HomePod, BoomCast steps aside. When the phone stops (pause or disconnect), a countdown starts and the PC sound comes back by itself.
- **Stays out of the way.** Lives in the notification area with a small panel for switches and volume; can start with Windows.
- **28 languages**, light and dark theme.

## Requirements

- Windows 10 or 11, 64-bit.
- Microsoft Edge WebView2 Runtime (already part of Windows 11 and of up-to-date Windows 10).
- A HomePod, HomePod mini or another AirPlay 2 speaker on the **same network** as the PC.
- In the Apple **Home** app: *Home Settings → Speakers & TVs → Allow Speaker & TV Access → Anyone on the Same Network*.

Developed and tested with a HomePod (2nd generation). Other AirPlay 2 speakers should work but have not been tested.

## Download and first start

1. Download `BoomCast.exe` from the [latest release](https://github.com/Lorenzo8484/BoomCast/releases/latest). There is nothing to install: put the file where you like and run it.
2. The file is not digitally signed, so Windows shows *"Windows protected your PC"*. Choose **More info → Run anyway**.
3. Your speakers appear under **Speakers**. Switch one on.
4. The first time, Windows Firewall must let the speaker's replies reach BoomCast: press **Allow in firewall** when the app asks and confirm the Windows prompt. This is needed once.

More detail, every setting explained and a troubleshooting list: **[User guide](docs/guide.md)**.

## Good to know

- **Dropouts on Wi-Fi.** With a very low delay a packet lost on Wi-Fi cannot be recovered in time and you hear a click. If it happens, raise the delay or keep ALAC compression on.
- **Translations** were produced automatically and have not been reviewed by native speakers. The log is in Italian.
- **Privacy.** BoomCast talks only to the speakers on your local network. It collects nothing and sends nothing to the Internet. Settings stay on your PC, in `%APPDATA%\BoomCast`.
- BoomCast speaks AirPlay 2 without Apple's involvement, so a future update of the speaker's software may stop it from working until BoomCast is updated.

## Problems and suggestions

Open an [issue](https://github.com/Lorenzo8484/BoomCast/issues). Say which speaker you have, your Windows version, and attach the text of *Settings → Log*.

## Rights and disclaimer

© 2026 Lorenzo. All rights reserved. BoomCast is free for personal use; it may not be modified, redistributed or sold without the author's written permission. It is provided "as is", without warranty of any kind: you use it at your own risk. Full terms: [LICENSE.md](LICENSE.md).

The source code is not published. BoomCast includes open-source libraries, listed with their licences in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
