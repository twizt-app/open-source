<h1 align="center">Twizt: open-source components</h1>

<p align="center">
  The complete source of the open-source components inside Twizt, for every version.
</p>

<p align="center">
  <a href="https://twizt.app">twizt.app</a> ·
  <a href="https://twizt.app/source/">Source code page</a> ·
  <a href="../../releases">Releases</a>
</p>

---

Twizt's own code is proprietary, but the app is built on open-source software
too. Its video player and its sound decoders are licensed under the GNU LGPL,
and that licence gives you the right to their complete source code, as Twizt
builds them. This repository is where that source lives.

## What's here

Each Twizt version has its own **release** in this repository, named after the
version (for example `0.9.0`). A release holds:

| Component | What it does in Twizt | Licence | Files |
|---|---|---|---|
| **libVLC** | The video player | LGPL-2.1-or-later | `vlc-android-*.tar.gz`: vlc-android, libvlcjni and VLC at the tag and commits Twizt builds, with Twizt's patches applied<br>`vlc-android-*.commits`: those tags, commits and patches<br>`vlc-contrib-tarballs-*.tar`: the original source of each library built into it (`vlc-contrib-packages-*.txt` names them)<br>`libvlc-build.tar.gz`: the build scripts |
| **FFmpeg audio decoders** | Dolby Digital, Dolby Digital Plus, TrueHD and DTS sound, through Media3 | LGPL-2.1-or-later | `ffmpeg-*.tar.gz`: the FFmpeg commit Twizt builds<br>`media3-*-decoder_ffmpeg.tar.gz`: Media3's decoder module<br>`media3-ffmpeg-build.tar.gz`: the build script |

Every release also has a `README.md` describing its files, and a `SHA256SUMS`
file with each file's checksum.

libVLC and the FFmpeg decoders are built **without** their GPL parts; their
build scripts show exactly which options are used.

## Checking a download

```bash
sha256sum -c SHA256SUMS          # Linux
shasum -a 256 -c SHA256SUMS      # macOS
```

## Building it yourself

Each component's build archive (`libvlc-build` or `media3-ffmpeg-build`) holds
the script Twizt builds it with. The script names the exact tag or commit and
every option used, and its comments list what the build needs.

## How long it stays

Each release stays here for at least **three years** after the last Twizt
version that ships it.

## Licences

Each component keeps its own licence, included in its source tree:
[GNU LGPL v2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html).

Every component in Twizt, open-source or not, is listed with its licence in the
app under **Settings → About → Open-source licences**.

## Questions

Open an issue on this repository, or write to
[legal@twizt.app](mailto:legal@twizt.app).
