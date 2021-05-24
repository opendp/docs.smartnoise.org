[![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)](https://opensource.org/licenses/MPL-2.0)
![CI](https://github.com/opendp/opendp-documentation/actions/workflows/main.yml/badge.svg)

# OpenDP Documentation

The OpenDP documentation is currently under development.

For users of SmartNoise, please visit these repositories:
 - The [SmartNoise Core Differential Privacy Library](https://github.com/opendp/smartnoise-core)
 - The accompanying [SmartNoise SDK repository](https://github.com/opendp/smartnoise-sdk) and 
 - For examples: [SmartNoise Samples repository](https://github.com/opendp/smartnoise-samples) 

## Dev Notes

```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
make html
open build/html/index.html
```

Docs are currently deployed to http://docs.opendp.org
