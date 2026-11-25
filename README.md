# Split MEG files

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Splits a CTF MEG recording into two time segments (for example test and retest) with MNE-Python and saves each as a .fif file.**

Reads the CTF .ds recording with mne.io.read_raw_ctf and saves two cropped copies: t1min-t1max to the test output and t2min-t2max to the retest output. Use it to cut one recording into two parts for test-retest analyses.

| | |
|---|---|
| 📥 **Inputs** | `neuro/meg/ctf` |
| 📤 **Outputs** | `neuro/meg/fif` ×2 |
| 🐳 **Container** | `brainlife/mne:0.23dev` |
| ⚙️ **Resources** | 8 CPUs |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.536](https://doi.org/10.25663/brainlife.app.536) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `fif file` | `neuro/meg/ctf` | yes | CTF MEG recording (.ds) with BIDS sidecars. |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `out_dir1` | `neuro/meg/fif` | First segment (t1min to t1max) as meg.fif. |
| `out_dir2` | `neuro/meg/fif` | Second segment (t2min to t2max) as meg.fif. |

<details>
<summary><b>⚙️ Parameters</b> (4)</summary>

| Parameter | Type | Default | Description |
|---|---|---|---|
| `t1min` | number | `0` | Start time of the first segment. (s) |
| `t1max` | string |  | End time of the first segment. (s) |
| `t2min` | number |  | Start time of the second segment. (s) |
| `t2max` | number |  | End time of the second segment. (s) |

</details>

📚 **References used by this App:**
- Avesani P, et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6:69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

<!-- brainlife-app:end -->

[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.469-blue.svg)](https://doi.org/10.25663/brainlife.app.469)

This Brainlife App splits MEG files 

## Authors
- Guiomar Niso (guiomar.niso@ctb.upm.es)


### Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your publications and code reusing this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://grantome.com/grant/NIH/R01-EB030896-01)

## Citations
We kindly ask that you cite the following articles when publishing papers and code using this code. 

*brainlife.io Publishing and Apps*
Avesani, P., McPherson, B., Hayashi, S. et al. **The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services**. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

*MNE-Python package:*  
Gramfort A, Luessi M, Larson E, Engemann DA, Strohmeier D, Brodbeck C, Goj R, Jas M, Brooks T, Parkkonen L, and Hämäläinen MS.  
**MEG and EEG data analysis with MNE-Python**  
Frontiers in Neuroscience, 7(267):1–13, 2013. https://doi.org/10.3389/fnins.2013.00267
      
  --

#### MIT Copyright (c) 2021 brainlife.io The University of Texas at Austin and Indiana University
