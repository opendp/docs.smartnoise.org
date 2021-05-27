[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![CI](https://github.com/opendp/opendp-documentation/actions/workflows/main.yml/badge.svg)

# OpenDP Documentation

The OpenDP documentation is currently under development.

For users of SmartNoise, please visit these repositories:
 - The [SmartNoise Core Differential Privacy Library](https://github.com/opendp/smartnoise-core)
 - The accompanying [SmartNoise SDK repository](https://github.com/opendp/smartnoise-sdk) and 
 - For examples: [SmartNoise Samples repository](https://github.com/opendp/smartnoise-samples) 

## Building the Docs

```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
make html
open build/html/index.html
```

## Deployment

Docs are deployed to http://docs.opendp.org using GitHub Actions.

Note that `make html` is replaced with `make versions` to build multiple versions (branches, tags) using the [sphinx-multiversion][] extension.

[sphinx-multiversion]: https://holzhaus.github.io/sphinx-multiversion/
