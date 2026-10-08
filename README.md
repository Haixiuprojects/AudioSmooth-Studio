# AudioSmooth Studio

**Offline vocal isolation and cleanup for Windows and Android.**

**By Filipino Developer — [@Haixiuprojects](https://github.com/Haixiuprojects)**

AudioSmooth Studio separates vocal estimates from music and can reduce echo/reverb locally. The Windows edition is a portable package with its own Python runtime. The Android edition is a native app with a verified model pack selected on-device. Neither build sends audio to a cloud service.

## Downloads

Use the matching GitHub Release and verify downloaded files with its `SHA256SUMS.txt`.

- [Windows v1.1.0 release](https://github.com/Haixiuprojects/AudioSmooth-Studio/releases/tag/windows-v1.1.0) — portable Windows 10/11 x64 ZIP, about 621.6 MiB.
- [Android v1.0.0 release](https://github.com/Haixiuprojects/AudioSmooth-Studio/releases/tag/android-v1.0.0) — APK (about 88.2 MiB) plus custom model sidecar (about 326.9 MiB).

## Windows quick start

1. Download and extract the complete ZIP; do not run it from the archive preview.
2. Double-click `Run_AudioSmooth.bat`.
3. Choose an audio file and workflow in the local browser interface.

The bundle includes CPython 3.12.10, pre-unpacked CPU packages, FFmpeg, and HQ3, DeEcho-DeReverb, and Karaoke-2 model assets. No `pip install`, CUDA, or system-wide Python setup is needed. The interface is local-only on `127.0.0.1`.

## Android quick start

1. Install the APK using Android's sideload flow.
2. Keep `main.1.com.audiosmooth.studio.obb` in Downloads; do not extract or rename it.
3. Open AudioSmooth Studio, tap **Choose offline model pack**, and select the `.obb` in the file picker.

The `.obb` is an AudioSmooth-specific `ASOBB1` sidecar, not a standard Android expansion file. Do not move it into `Android/obb`. The APK has no Android `INTERNET` permission. See the [Android install guide](docs/Android_Install_Guide.md).

## Workflows

- **Split + Clean vocal:** isolate vocals and accompaniment, apply additional same-model cleanup, then reduce echo/reverb; optional gentle polish.
- **Split vocals only:** one main vocal/music separation with adaptive bleed reduction, DeEcho-DeReverb, and optional light polish; produces a cleaned vocal result.
- **Clean Voice Only:** clean echo/reverb from an already isolated voice; it does not split instruments from a full song.
- **Lead & Back Vocal Splitter:** isolate the combined vocal and estimate lead and backing vocals.

Windows supports common audio formats and inputs up to 256 MB. Android supports up to 6 minutes and 256 MB per input. Outputs are WAV.

## Privacy and quality

Audio processing runs locally after download/setup. CPU speed, memory use, and processing time vary by PC or phone. Vocal/music separation is an estimate: difficult mixes, percussion, backing vocals, distortion, clipping, and strong reverb can leave residue or affect vocal timbre. **Zero instrumental bleed is not guaranteed for every track.** Keep the original and compare the outputs.

The user reported a successful Android-phone run that sounded like their Windows result. This is informal feedback from one unspecified device, not a compatibility or performance benchmark across Android devices.

## Third-party components

The downloadable builds contain third-party software and neural model weights. Their terms and attributions are distinct; see [Third-party notices](THIRD_PARTY_NOTICES.md) and the notices included in the Windows package. The maintainer confirms authorization for the model-containing assets in these releases; use the models in accordance with their applicable upstream terms.

## Repository contents and license

This public repository is a **binary release and documentation hub**. It does not currently publish the full application source code and does not grant a source-code license. Do not treat the binaries as an open-source code release.
