# OpenDP Links
(in progress)
Links related to OpenDP development

## Public websites:
- [privacytools.seas.harvard.edu/opendp](https://privacytools.seas.harvard.edu/opendp) (HU Privacy Tools Project)
- [opendp.io](https://projects.iq.harvard.edu/opendp)
- [opendifferentialprivacy.github.io](http://opendifferentialprivacy.github.io/) (forwards to smartnoise)
- [smartnoise.org](smartnoise.org)

## Project tracking

- [Weekly OpenDP Meeting Agenda/Notes](https://docs.google.com/document/d/10M5EceKtSAWA0czgIpLYG2jxCbzgXyKxT0HQjqvFdlQ/edit)
- [MVP Project Board](https://github.com/orgs/opendifferentialprivacy/projects/2)
  - GitHub issue tracking across several repositories.
- [Miro Boards](https://miro.com/):
  - [Timeline](https://miro.com/app/board/o9J_kiQ6j90=/)
  - [MVP UX Workflow](https://miro.com/app/board/o9J_kj6tycQ=/)
  - [MVP Testing](https://miro.com/app/board/o9J_kiOSrqU=/)
  - [Project Constituents](https://miro.com/app/board/o9J_kiAGSws=/)
- [MVP Google Drive](https://drive.google.com/drive/u/1/folders/0AHJNRfEnaIS2Uk9PVA)
  - [PSI Collaboration Google Drive](https://drive.google.com/drive/u/1/folders/0AL0Zu-Y8rawGUk9PVA) (older)

## GitHub Repositories

The GitHub repositories are located located under the organization ["opendifferentialprivacy"](https://github.com/opendifferentialprivacy)
- **opendifferentialprivacy**: [GitHub org](https://github.com/opendifferentialprivacy)


## OpenDP

  - **OpenDP-Experimental**: [code](https://github.com/opendifferentialprivacy/OpenDP-Experimental) | [issues](https://github.com/opendifferentialprivacy/OpenDP-Experimental/issues)
    - New library, under development.
    - [Architecture Notes (google drive)](https://drive.google.com/drive/u/1/folders/1KBLbpg8G2jGstaCCqWXYw0sf9F1IR6Rn) | [Architecture Questions](https://docs.google.com/document/d/11ZX0Zb3XxVQdtXrkgIf4pwiay-IiH0x8iaa5NpHRCWA/edit)
    - (Repository name to be changed.)
  - **opendp-ux**: [code](https://github.com/opendifferentialprivacy/opendp-ux) | [issues](https://github.com/opendifferentialprivacy/opendp-ux/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/opendp-ux)
    - Miro: [Data models](https://miro.com/app/board/o9J_kjGaN7E=/) | [Input/Output](https://miro.com/app/board/o9J_kiJHr4g=/)
    - OpenDP App for the MVP.
    - Depositor/Analyst workflows.
  - **opendp-schemas**: [code](https://github.com/opendifferentialprivacy/opendp-schemas) | [issues](https://github.com/opendifferentialprivacy/opendp-schemas/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/opendp-schemas)
    - Schemas for OpenDP. Repository may be used as submodule.
    - Includes the release schemas. Will contain code for converting release schemas to other formats (PDF reports, DDI XML, etc.)


## SmartNoise

SmartNoise currently includes several inter-related repositories.

  - **smartnoise-core**: [code](https://github.com/opendifferentialprivacy/smartnoise-core) | [issues](https://github.com/opendifferentialprivacy/smartnoise-core/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/smartnoise-core)
    - Initial OpenDP library in Rust. Previous names: smartnoise-core; yarrow
    - Rust crates:
        - [smartnoise_validator](https://crates.io/crates/smartnoise_validator)
        - [smartnoise_runtime](https://crates.io/crates/smartnoise_runtime)
    - Previous names: whitenoise-core-python, yarrow
    - To eventually be replaced with **OpenDP-Experimental**

  - **smartnoise-core-python**: [code](https://github.com/opendifferentialprivacy/smartnoise-core-python) | [issues](https://github.com/opendifferentialprivacy/smartnoise-core-python/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/smartnoise-core)
    - Python bindings to **smartnoise-core**
        - PyPI: [opendp-smartnoise-core](https://pypi.org/project/opendp-smartnoise-core/)
    - Previous name: whitenoise-core-python
  - **smartnoise-sdk**: [code](https://github.com/opendifferentialprivacy/smartnoise-sdk) | [issues](https://github.com/opendifferentialprivacy/smartnoise-sdk/issues)
    - Tools and services for DP processing of tabular and relational data
    - Uses python bindings from **smartnoise-core-python**
    - Previous name: whitenoise-system; burdock
  - **smartnoise-samples**: [code](https://github.com/opendifferentialprivacy/smartnoise-samples) | [issues](https://github.com/opendifferentialprivacy/smartnoise-samples/issues)
    - Includes Jupyter notebook examples
    - Depending on the examples uses python bindings from **smartnoise-core-python** and/or **smartnoise-sdk**
    - Previous name: smartnoise-samples
  - **smartnoise.org**: [code](https://github.com/opendifferentialprivacy/smartnoise.org) | [website](https://smartnoise.org)
    - Informational site