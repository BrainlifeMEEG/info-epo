# Create an info text file

[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.818-blue.svg)](https://doi.org/10.25663/brainlife.app.818)

## Description

This Brainlife.io app reads the `.info` attribute of an MNE `Epochs` object (loaded with `mne.read_epochs`) and writes it to a text file for easy viewing, surfacing the same summary in `product.json` for quick inspection without downloading the file.

The app generates:
- A text dump of the epoched data's `.info` attribute
- A `product.json` message containing the same info summary

## Inputs

- **`epo`** (`neuro/meeg/mne/epochs`): epoched MEG/EEG data whose `.info` attribute is read (required)

## Outputs

- **`out_dir/info.txt`** (`neuro/meg/fif-override`, tag `info`): text dump of the epochs' `.info` attribute
- **`product.json`**: message containing the same info summary, displayed in the Brainlife.io process view

## Configuration Parameters

This app reads no configuration parameters beyond its input file (see Inputs above).

## Usage

### Running on Brainlife.io

1. Select your epoched MEG/EEG dataset as the `epo` input.
2. Submit the process.
3. Inspect `info.txt` and the `product.json` summary in the process viewer.

### Local Testing

```bash
# Edit config.json to point "epo" at real epoched data, then:
python main.py
```

## Authors

- Kamilya Salibayeva (https://github.com/KSalibay)

## Citations

We kindly ask that you cite the following articles when publishing papers and code using this app:

- Hayashi, S., Caron, B.A., Heinsfeld, A.S. et al. brainlife.io: a decentralized and open-source cloud platform to support neuroscience research. Nat Methods 21, 809–813 (2024). https://doi.org/10.1038/s41592-024-02237-2
- Gramfort, A. et al. MEG and EEG data analysis with MNE-Python. Front. Neurosci. 7, 267 (2013). https://doi.org/10.3389/fnins.2013.00267
- Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). https://doi.org/10.1038/s41597-019-0073-y

## Funding Acknowledgement

brainlife.io is publicly funded and for the sustainability of the project it is helpful to acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your publications and code reusing this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://grantome.com/grant/NIH/R01-EB030896-01)

## License

Copyright (c) 2026 MEEG Brainlife team. Licensed under AGPL-3.0, see [license.txt](license.txt).
