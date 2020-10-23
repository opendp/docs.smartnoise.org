# OpenDP Links

Links related to OpenDP development. (In progress)
- [Public websites](#public-websites)
- [Project tracking](#project-tracking)
- [UX](#ux)
- [GitHub Repositories](#github-repositories)
  - [OpenDP Repositories](#opendp-repositories)
  - [SmartNoise Repositories](#smartnoise-repositories)
- [GSuite emails/users](#gsuite-emailsusers)

## Public websites:
- [privacytools.seas.harvard.edu/opendp](https://privacytools.seas.harvard.edu/opendp) (HU Privacy Tools Project)
- [opendp.io](https://projects.iq.harvard.edu/opendp)
- [opendifferentialprivacy.github.io](http://opendifferentialprivacy.github.io/) (forwards to smartnoise)
- [smartnoise.org](smartnoise.org)


## Project tracking

- [Weekly OpenDP Meeting Agenda/Notes](https://docs.google.com/document/d/10M5EceKtSAWA0czgIpLYG2jxCbzgXyKxT0HQjqvFdlQ/edit)
  - [Business Process Diagram](https://drive.google.com/file/d/1YAWzwNVMiEtbBljdUe96dT9uPpYHJBqK/view)
- [MVP Project Board](https://github.com/orgs/opendifferentialprivacy/projects/2)
  - GitHub issue tracking across several repositories.
- [Miro Boards](https://miro.com/):
  - [Timeline](https://miro.com/app/board/o9J_kiQ6j90=/)
  - [MVP UX Workflow](https://miro.com/app/board/o9J_kj6tycQ=/)
  - [MVP Testing](https://miro.com/app/board/o9J_kiOSrqU=/)
  - [Project Constituents](https://miro.com/app/board/o9J_kiAGSws=/)
- [MVP Google Drive](https://drive.google.com/drive/u/1/folders/0AHJNRfEnaIS2Uk9PVA)
  - [PSI Collaboration Google Drive](https://drive.google.com/drive/u/1/folders/0AL0Zu-Y8rawGUk9PVA) (older)

## UX
  - Miro: [MVP UX Workflow](https://miro.com/app/board/o9J_kj6tycQ=/)
  - [Wireframes (videos)](https://drive.google.com/drive/u/1/folders/1IFE8mmcCg4ROomP-ADWvdaZzJgutmgdj)
  - [Consolidated User Feedback](https://docs.google.com/presentation/d/1_BNWqttrkqzUCcubh5zYtLyir97Lj4lzBbS6SMz9QaE/edit#slide=id.p)

## GitHub Repositories

The GitHub repositories are located located under the organization ["opendifferentialprivacy"](https://github.com/opendifferentialprivacy)
- **opendifferentialprivacy**: [GitHub org](https://github.com/opendifferentialprivacy)


## OpenDP Repositories

  - **OpenDP-Experimental**: [code](https://github.com/opendifferentialprivacy/OpenDP-Experimental) | [issues](https://github.com/opendifferentialprivacy/OpenDP-Experimental/issues)
    - New library, under development. (Repository name to be changed.)
    - Statistics:
        - [Components, prioritized](https://docs.google.com/spreadsheets/d/132rAzbSDVCKqFZWeE-P8oOl9f23PzkvNwsrDV5LPkw4/edit#gid=0)
        - [For MVP App](https://docs.google.com/spreadsheets/d/1L-LWTf7PMZBbCuQxSbAFQkZKEtb6AgsK3qF6lwY_xrA/edit#gid=0)
    - [Architecture Notes (google drive)](https://drive.google.com/drive/u/1/folders/1KBLbpg8G2jGstaCCqWXYw0sf9F1IR6Rn) | [Architecture Questions](https://docs.google.com/document/d/11ZX0Zb3XxVQdtXrkgIf4pwiay-IiH0x8iaa5NpHRCWA/edit)
  - **opendp-ux**: [code](https://github.com/opendifferentialprivacy/opendp-ux) | [issues](https://github.com/opendifferentialprivacy/opendp-ux/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/opendp-ux)
    - Miro: [Data models](https://miro.com/app/board/o9J_kjGaN7E=/) | [Input/Output](https://miro.com/app/board/o9J_kiJHr4g=/)
    - OpenDP App for the MVP.
    - Depositor/Analyst workflows.
  - **opendp-schemas**: [code](https://github.com/opendifferentialprivacy/opendp-schemas) | [issues](https://github.com/opendifferentialprivacy/opendp-schemas/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/opendp-schemas)
    - Schemas for OpenDP. Repository may be used as submodule.
    - Includes the release schemas. Will contain code for converting release schemas to other formats (PDF reports, DDI XML, etc.)
  - **dp-test-datasets**: [code](https://github.com/opendifferentialprivacy/dp-test-datasets) | [issues](https://github.com/opendifferentialprivacy/dp-test-datasets/issues)

## SmartNoise repositories

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

## GSuite users

- [GSuite](https://admin.google.com/) for opendp.io:
  - admin@opendp.io  - admin account, billing, etc
  - comms@opendp.io
  - community@opendp.io - forwards to opendp-community@g.harvard.edu
  - smartnoise@opendp.io - forwards to smartnoise-support slack channel
  - whitenoise@opendp.io - forwards to smartnoise-support slack channel
    - (will be removed)
