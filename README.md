# Qopen: Separation of intrinsic attenuation and scattering, site and source terms

## Qopen practical using the 2019 Ridecrest Earthquake Sequence dataset

*Author: Tom Eulenfeld*

Qopen can be used to estimate the scattering and intrinsic contributions to the attenuation for a local to regional dataset.  In addition, Qopen can be used to estimate relative site gains as a function of frequency and to estimate source spectra and source parameters, i.e., seismic moment, moment magnitude, corner frequency, and stress drop, for small to moderate earthquakes.

This notebook was created for the 13th Munich Earth Skience School (2023).

### Dataset

The dataset used in this notebook and included in the repository is available at https://scedc.caltech.edu/data/stressdrop-ridgecrest.html
and was used as a benchmark in the "Community Stress Drop Validation Study using the 2019 Ridgecrest Earthquake Sequence".

Dataset References:
 * Baltay, A., Abercrombie, R. E., Taira, T. (2021), A Community Stress Drop Validation Study Using the 2019 Ridgecrest Earthquake Dataset, SSA Annual Meeting 2021.
 * Trugman, D. T. (2020), Stress‐Drop and Source Scaling of the 2019 Ridgecrest, California, Earthquake Sequence. Bulletin of the Seismological Society of America 2020; 110 (4): 1859–1871. doi: 10.1785/0120200009
 * Baltay, A. S., R. E. Abercrombie, T. Taira, A community stress drop validation study using the 2019 Ridgecrest Earthquake Sequence, Seismological Research Letters (in preparation)

The dataset consists of 56 earthquakes from the 2019 earthquake sequence. For most of this practical, we will use 8 selected events from these 56 events. Out of the 34 stations provided in the inventory, we will only use 6 stations to limit the runtime of Qopen

### Setup

To work through the practical, please download or clone this repository.
You will need the following Python packages: `jupyter obspy qopen cartopy`.
For ObsPy versions `<1.5` you will additionally need the package `obspycsv`.
Finally, start the Jupyter notebook server with `jupyter notebook`.
One of many possibilities for installation is via conda:

```
conda create -c conda-forge -n practical jupyter obspy cartopy statsmodels
conda activate practical
pip install qopen
#pip install obspycsv  # for ObsPy<1.5
jupyter notebook
```

### Topics

The notebook covers the following topics:

1. Plot event catalog with ObsPy and in a custom plot including depth sections
2. Plot waveforms and calculate the seismic envelope and spectral energy density
3. Understand impact of intrinsic attenuation and scattering on the seismic envelope
4. Use Qopen to estimate intrinsic attenuation and scattering strength for a local dataset, load and plot results
5. Calculate coda Q for one event-station pair and compare it with the Q estimates for scattering and intrinsic attenuation
5. Estimate basic source parameters including the moment magnitude

Answers and code updates can be directly inserted into this notebook.

The slides of an introductory talk presented at the 2023 Skience workshop are located in this repository.
Additional resources are listed in the [Qopen repository](https://github.com/trichter/qopen).
Get help in the [Qopen category of the ObsPy forum](https://discourse.obspy.org/c/obspy-related-projects/qopen/15).
Bugs can be reported in the issue tracker of this repository.
