# opendp-docs-proposals
## Build

1. Clone the repo and `cd` into the directory. `git clone https://github.com/opendifferentialprivacy/opendp-documentation.git && cd opendp-documentation`
1. Create virtual environment: `python3 -m venv venv`
1. Activate virtual environment: `. venv/bin/activate`
2. Install requirements: `pip install -r requirements.txt`
3. Move static files: `rsync -avz static/ sphinx-opendp/_static/`
4. Move templates: `rsync -avz template/ sphinx-opendp/_templates/`
5. Build html: `cd sphinx-opendp && make clean && make html`

