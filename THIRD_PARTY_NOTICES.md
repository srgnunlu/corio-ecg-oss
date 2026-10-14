# Third-party notices

The root MIT license applies to original Corio ECG contributions. It does not
relicense upstream source, patches containing upstream context, model weights,
datasets, or their derived artifacts.

| Component | Relationship | Applicable notice |
| --- | --- | --- |
| [ECGFounder](https://github.com/PKUDigitalHealth/ECGFounder) | `src/models/net1d.py` adapts the upstream architecture while preserving checkpoint key names. | MIT, copyright 2025 PKUDigitalHealth; full notice in `LICENSES/ECGFounder-MIT.txt`. |
| [Open-ECG-Digitizer](https://github.com/Ahus-AIM/Open-ECG-Digitizer) | Downloaded separately. The compatibility patch in `vendor/patches/open-ecg-digitizer.patch` contains upstream context and Corio modifications; that patch is offered under CC BY-SA 4.0. | Full text in `LICENSES/Open-ECG-Digitizer-CC-BY-SA-4.0.txt`. |
| [ECG-Image-Kit](https://github.com/alphanumericslab/ecg-image-kit) | Downloaded separately for synthetic image generation. Its subcomponents may carry additional licenses. | BSD-3-Clause at the pinned revision; root notice in `LICENSES/ECG-Image-Kit-BSD-3-Clause.txt`. Preserve subcomponent notices in any separate redistribution. |
| [ECG-Digitiser](https://github.com/felixkrones/ECG-Digitiser) | Optional upstream digitization backend; not bundled. | BSD-2-Clause; notice in `LICENSES/ECG-Digitiser-BSD-2-Clause.txt`. |

The Open-ECG-Digitizer patch is based on revision
`963387ff5abdfa3db91c15ac52d6cf1214345a6a`. Setup pins
`9e712feac158d127843faac7d5e100ced00d0e6e`, which adds the upstream license.
The compared revision changes comprise `LICENSE`, type-checker configuration
in `pyproject.toml`, and a minimal `uv.lock`; executable Python source is unchanged.
The patch itself documents each modification in unified-diff form.

Model weights are downloaded by the user and are not included in this source
distribution. The official [ECGFounder model card](https://huggingface.co/PKUDigitalHealth/ECGFounder)
identifies the weights as MIT. Check the applicable source terms for each
additional model or dataset before use or redistribution.

No ECG recordings, patient-level benchmark exports, clinical photographs,
trained weights, or private development notes are included in this package.
Download scripts do not grant permission to redistribute the downloaded data.
