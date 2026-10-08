# AudioSmooth Studio for Windows — v1.1.0

**By Filipino Developer — [@Haixiuprojects](https://github.com/Haixiuprojects)**

A portable, CPU-only vocal isolation and cleanup application for Windows 10/11 x64. The complete ZIP includes CPython 3.12.10, pre-unpacked dependencies, FFmpeg, and the required model assets. No `pip install`, system-wide Python setup, CUDA, account, or cloud audio upload is needed.

## Workflows

- **Split + Clean vocal:** separates vocal and accompaniment; uses same-model iterative cleanup (up to six passes, stopping earlier if the configured instrumental-stem proxy threshold is met), adaptive masking, DeEcho-DeReverb, and optional light polish. Intermediate WAV stems are saved for comparison.
- **Split vocals only:** one primary separation, adaptive bleed reduction, DeEcho-DeReverb, and optional light polish. Main result: cleaned vocal WAV.
- **Clean Voice Only:** reduce echo/reverb in an already isolated voice; does not remove instruments from a complete song.
- **Lead & Back Vocal Splitter:** isolate the combined vocal and estimate lead and backing vocals using the included Karaoke-2 model.

Inputs: common audio formats, up to 256 MB. Outputs: WAV. Recommended: Windows 10/11 x64 and 8 GB RAM or more; CPU time varies with the track and machine.

## Install

Download the full ZIP from the [Windows release](https://github.com/Haixiuprojects/AudioSmooth-Studio/releases/tag/windows-v1.1.0), extract all files, and run `Run_AudioSmooth.bat`. Keep the folders together. Audio is processed locally; the app binds to `127.0.0.1` only.

## Quality

Separation is an estimate, not a promise of mathematically zero bleed. Dense arrangements, drums, backing vocals, clipping, distortion, or strong reverb can leave residue or affect vocal timbre. Keep the original audio and compare the outputs.

The maintainer confirms authorization to distribute the model assets included in this release. See [third-party notices](../THIRD_PARTY_NOTICES.md) and follow upstream model terms.
