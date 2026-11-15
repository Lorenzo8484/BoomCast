# Changelog

## 0.11

Fixes found in a full review of 0.10. No new features.

- The app could close by itself when the tray panel was taller than the screen (many speakers on a small display).
- Saving a sound mode while another one was active could attach later changes to the wrong mode.
- A sound mode you saved no longer switches the audio enhancements off or changes balance, limiter and dithering: it holds only its own sound.
- A speaker lent to a phone is no longer taken back while the phone is still playing if it briefly drops off the network.
- Switching a speaker on, off and on again quickly now ends with it on.
- A slider being held is no longer moved back by an update from the app; the speaker list keeps updating after a click on a volume slider.
- Settings are saved safely: a crash while saving can no longer reset them.
- The page title follows the language when it is changed; status values are no longer cut off in languages with long words.
- The tray panel no longer reopens when right-clicking the icon to close it.

## 0.10

First public version.

- PC audio to HomePod and other AirPlay 2 speakers, several at once.
- Delay from 0.15 s; ALAC or PCM, 44.1 kHz / 16 bit lossless.
- 10-band equaliser, spatial sound and dynamics; nine sound modes, user modes with free names, per-mode memory and reset, drag to reorder.
- Live level meters by band and by channel.
- Steps aside when a phone plays on the speaker and comes back after a countdown.
- Notification-area panel, start with Windows.
- 28 languages, light and dark theme.
