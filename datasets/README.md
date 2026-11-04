# CSI Datasets

This directory contains six DeepMIMO-based high-resolution CSI datasets from New York (NY), Los Angeles (LA), and Chicago (CHI).

## Files and Array Format

| File | City | Transmit antennas (N_T) | Users (K) | H_gather shape |
| --- | --- | --- | --- | --- |
| [NY_ant16_user8.mat](NY_ant16_user8.mat) | NY | 16 | 8 | `(10000, 8, 16)` |
| [NY_ant32_user16.mat](NY_ant32_user16.mat) | NY | 32 | 16 | `(10000, 16, 32)` |
| [LA_ant16_user8.mat](LA_ant16_user8.mat) | LA | 16 | 8 | `(10000, 8, 16)` |
| [LA_ant32_user16.mat](LA_ant32_user16.mat) | LA | 32 | 16 | `(10000, 16, 32)` |
| [CHI_ant16_user8.mat](CHI_ant16_user8.mat) | CHI | 16 | 8 | `(10000, 8, 16)` |
| [CHI_ant32_user16.mat](CHI_ant32_user16.mat) | CHI | 32 | 16 | `(10000, 16, 32)` |

Each file is a MATLAB `.mat` file containing one variable, **`H_gather`**. Its dimensions are ordered as:

```text
(number of samples, number of users, number of transmit antennas)
```

Values are stored as complex single-precision numbers (`complex64` in NumPy). The stored per-sample array has shape `(K, N_T)`; the paper's channel matrix convention is `N_T × K`.

## Sample Selection

Each released dataset contains the **last 10,000 samples** of its corresponding original 100,000-sample dataset, preserving the original order. Specifically:

- MATLAB sample indices: `90001:100000`.
- Python sample slice: `[90000:100000, :, :]`.
- No shuffling, normalization, or other preprocessing was applied during this extraction.
- Original variable names, array axis order, and numerical precision are preserved.

The files contain the selected CSI arrays without separate training, validation, or test labels. The manuscript describes an 8,000/1,000/1,000 training/validation/test ratio; this release does not encode the original split indices. See [manifest.json](manifest.json) for the source filenames, shapes, selection details, and file checksums.

## MATLAB Example

Run from the repository root:

```matlab
S = load('datasets/NY_ant16_user8.mat');
H_gather = S.H_gather;
size(H_gather)                   % 10000 x 8 x 16
H_sample = squeeze(H_gather(1, :, :)); % 8 x 16, users x antennas
H = H_sample.';                  % 16 x 8; non-conjugating transpose
```

## Python Example

The following example uses NumPy and SciPy. Run from the repository root:

```python
from scipy.io import loadmat

H_gather = loadmat('datasets/NY_ant16_user8.mat')['H_gather']
print(H_gather.shape)   # (10000, 8, 16)
print(H_gather.dtype)   # complex64
H_sample = H_gather[0]  # (8, 16), users x antennas
H = H_sample.T         # (16, 8); non-conjugating transpose
```

## Data Source

The channel samples are derived from [DeepMIMO](https://www.deepmimo.net/). Original source filenames and base-station identifiers are recorded in [manifest.json](manifest.json).
