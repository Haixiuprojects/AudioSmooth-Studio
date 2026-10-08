# Third-party notices

AudioSmooth Studio's Windows and Android releases bundle third-party software, model weights, and runtime components. Each component may have terms separate from AudioSmooth's release documentation. The project maintainer confirms authorization to distribute the model assets included in these specific releases; users must still follow applicable upstream terms and attribution requirements.

## Vocal-separation models

- Ultimate Vocal Remover model repository: [TRvlvr/model_repo](https://github.com/TRvlvr/model_repo/releases/tag/all_public_uvr_models)
- Included model families: UVR-MDX-NET-Inst_HQ_3; UVR-DeEcho-DeReverb; UVR_MDXNET_KARA_2.
- The model weights are not covered automatically by the license of the application/library code. Consult upstream model documentation for attribution and use terms.

## Audio Separator

- [nomadkaraoke/python-audio-separator](https://github.com/nomadkaraoke/python-audio-separator) — MIT-licensed project, according to its upstream repository.
- The Windows ZIP retains package metadata and license material for bundled dependencies where supplied.

## Runtime and Android dependencies

- Windows bundles the CPython 3.12.10 embeddable distribution from [python.org](https://www.python.org/ftp/python/3.12.10/) under the Python Software Foundation license, plus dependency metadata/notices in the archive.
- Android includes ONNX Runtime and Android/Compose/audio-processing dependencies; consult the relevant dependency licenses and project notices for the versioned build.

This file is an attribution summary, not a substitute for any license or terms supplied with the upstream components.
