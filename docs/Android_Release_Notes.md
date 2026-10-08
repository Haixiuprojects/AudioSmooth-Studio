# AudioSmooth Studio for Android — v1.0.0

**By Filipino Developer — [@Haixiuprojects](https://github.com/Haixiuprojects)**

A native Android app for offline vocal isolation and cleanup. It runs ONNX models on-device after the local model pack has been selected. The APK does not request Android's `INTERNET` permission.

## Assets

Download from the [Android release](https://github.com/Haixiuprojects/AudioSmooth-Studio/releases/tag/android-v1.0.0):

- `AudioSmoothStudio_Android_v1.0.0.apk` — 92,519,925 bytes (~88.2 MiB).
- `main.1.com.audiosmooth.studio.obb` — 342,814,142 bytes (~326.9 MiB).
- `AudioSmoothStudio_Android_Install_Guide.md` and `SHA256SUMS.txt`.

## Install

1. Install the APK using Android's sideload flow.
2. Leave the `.obb` in Downloads; do not extract or rename it.
3. In AudioSmooth Studio, tap **Choose offline model pack** and select the `.obb` in the file picker.

The `.obb` uses AudioSmooth's custom `ASOBB1` format. It is not a standard Android expansion-file mount; do not move it to `Android/obb`. The app verifies the pack index and model hashes before loading. Minimum Android API: 26. The package includes ONNX Runtime libraries for ARM64, ARMv7, x86, and x86_64.

## Workflows and limits

Split + Clean vocal, Split vocals only, Clean Voice Only, and Lead & Back Vocal Splitter. Results are WAV. The mobile app limits each input to six minutes and 256 MB. Processing speed and memory use vary by device.

The project builds successfully and two JVM DSP tests pass. The user reported successful processing on one Android phone with sound comparable to Windows; this is informal feedback, not broad-device benchmarking. Separation quality varies by source; literal zero bleed is not guaranteed.

This APK is debug-signed for sideloaded evaluation, not Google Play. The maintainer confirms authorization to distribute the model pack included in this release; follow applicable upstream model terms.
