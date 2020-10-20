# OpenDP Links
(in progress)
Links related to OpenDP development

## Project tracking

- [MVP Project Board](https://github.com/orgs/opendifferentialprivacy/projects/2)
  - GitHub issue tracking across several repositories.

## GitHub Repositories

The GitHub repositories are located located under the organization ["opendifferentialprivacy"](https://github.com/opendifferentialprivacy) 
- **opendifferentialprivacy**: [GitHub org](https://github.com/opendifferentialprivacy) 


## OpenDP 

  - **OpenDP-Experimental**: [code](https://github.com/opendifferentialprivacy/OpenDP-Experimental) | [issues](https://github.com/opendifferentialprivacy/OpenDP-Experimental/issues)
    - New library, under development. 
    - (Repository name to be changed.)
  - **opendp-ux**: [code](https://github.com/opendifferentialprivacy/opendp-ux) | [issues](https://github.com/opendifferentialprivacy/opendp-ux/issues) | [TravisCI](https://travis-ci.com/github/opendifferentialprivacy/opendp-ux)
    - OpenDP App for the MVP. 
    - Depositor/Analyst workflows.
  - **opendp-schemas**: [code](https://github.com/opendifferentialprivacy/opendp-schemas) | [issues](https://github.com/opendifferentialprivacy/opendp-schemas/issues)
    - Schemas for OpenDP. Repository may be used as submodule.
    - Includes the release schemas. Will contain code for converting release schemas to other formats (PDF reports, DDI XML, etc.)


## SmartNoise 

SmartNoise currently includes 4 inter-related repositories which build upon each other. 

  - **smartnoise-core**: [code](https://github.com/opendifferentialprivacy/smartnoise-core) | [issues](https://github.com/opendifferentialprivacy/smartnoise-core/issues)
    - Initial OpenDP library in Rust. Previous names: smartnoise-core; yarrow
    - Rust crates:
        - [smartnoise_validator](https://crates.io/crates/smartnoise_validator)
        - [smartnoise_runtime](https://crates.io/crates/smartnoise_runtime)
    - Previous names: smartnoise-core-python, yarrow
    - To eventually be replaced with **OpenDP-Experimental**

  - **smartnoise-core-python**: [code](https://github.com/opendifferentialprivacy/smartnoise-core-python) | [issues](https://github.com/opendifferentialprivacy/smartnoise-core-python/issues)
    - Python bindings to **smartnoise-core**
        - PyPI: [opendp-smartnoise-core](https://pypi.org/project/opendp-smartnoise-core/)
    - Previous name: smartnoise-core-python
  - **smartnoise-system**: [code](https://github.com/opendifferentialprivacy/smartnoise-system) | [issues](https://github.com/opendifferentialprivacy/smartnoise-system/issues)
    - Tools and services for DP processing of tabular and relational data
    - Uses python bindings from **smartnoise-core-python**
        - PyPI: [opendp-smartnoise](https://pypi.org/project/opendp-smartnoise/)
          - (This packages includes **smartnoise-core-python**)
    - Previous name: smartnoise-system; burdock
  - **smartnoise-samples**: [code](https://github.com/opendifferentialprivacy/smartnoise-samples) | [issues](https://github.com/opendifferentialprivacy/smartnoise-samples/issues)
    - Includes Jupyter notebook examples
    - Depending on the examples uses python bindings from **smartnoise-core-python** and/or **smartnoise-system**
    - Previous name: smartnoise-samples
