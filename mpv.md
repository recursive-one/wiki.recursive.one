---
title: MPV
toc: no
categories: Linux
...

# MPV

Here you can find some tricks I use with [the MPV player](https://mpv.io/).

## VAAPI

To enable the [VAAPI](https://en.wikipedia.org/wiki/Video_Acceleration_API) (hardware acceleration) install a suitable package

```sh
$ sudo apt-get install i965-va-driver
```

and add to your `$HOME/.config/mpv/mpv.conf` this options

```ini
[default]
hwdec=auto
vo=gpu,x11
```

## Local configurations

The MPV can read a `mpv.conf` file from the directory that contains the files you want to play. This option can be pretty useful when you want to remember the selected audio track or the playback speed just for files in this particular directory. You even can set the options for a particular file: for `video.avi` put your stuff into `vide.avi.conf`. To enable this feature just add this to your config file:

```ini
[default]
use-filedir-conf=yes
```

## No display for audio

Sometimes I use MPV to play audio. Usually, MPV tries to display the album art in a separate window. But I prefer to keep this feature disabled with this option:

```ini
[default]
audio-display=no
```

## ytdl format

MPV can play video-streams using the [YTDL](https://yt-dl.org/). But by default the highest quality will be chosen. I prefer to limit the quality to 720p (or less) so I have this in my config:

```ini
[default]
ytdl-format=bestvideo[height<=?720]+bestaudio
```

More: ["MPV + youtube-dl: Stop Wasting Resources"](https://www.funkyspacemonkey.com/mpv-youtube-dl-stop-wasting-resources).