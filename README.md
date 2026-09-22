# WAKE-NET

WAKE-NET: Wake-Aware Wind Farm Layout and Sizing Optimization Framework

## Wake-Aware Economic Wind Farm Layout, Turbine Selection, and Cabling Optimization

This repository shares the Python implementation and example wind datasets associated with:

**Ann Mary Toms and Xingpeng Li**, "WAKE-NET: A 3D-wake-aware economic turbine layout and cabling optimization framework for multi-capacity multi-hub-height wind farms serving grid-scale and industrial power systems," *Renewable Energy*, vol. 273, article 126078, 2026.  

**DOI:** https://doi.org/10.1016/j.renene.2026.126078  
**Paper page:** https://rpglab.github.io/papers/AnnT-WakeNET/

This repository contains the Python implementation of WAKE-NET, a wake-aware wind farm optimization framework developed to maximize the economic performance of onshore and offshore wind farms. The framework simultaneously considers wind resource characteristics, wake interactions, turbine selection, turbine placement, and cable routing to determine optimal wind farm configurations.

The model utilizes historical wind speed and wind direction data together with the Jensen wake model to estimate wake-adjusted energy production and annual economic benefit.


### Python Jupyter Notebook

The code is implemented in Python using Jupyter Notebook.

* `WAKENET.ipynb` contains the complete workflow, including wind resource processing, wake modeling, turbine layout optimization, turbine selection, cable routing, economic evaluation, and visualization.
* `OnshoreIN_all.xlsx` contains the historical offshore wind observations for region `Onshore Indiana`.
* `OffshoreHI_all.xlsx` contains the historical onshore wind observations for region `Offshore Hawaii`.

## Input Wind Data Workbooks

Each Excel workbook contains one worksheet of time-stamped wind observations. The first row contains the variable names, the second row contains the corresponding descriptions or units, and the remaining rows contain the wind measurements.

| Column | Meaning |
| --- | --- |
| `Date` | Timestamp associated with the wind observation. This is stored as a date-time serial value and displayed using a date-time format.  |
| `YY`, `MM`, `DD`, `hh`, `mm` | Year, month, day, hour, and minute fields. |
| `WDIR` | Wind direction measured clockwise from true north. A value of 0° or 360° represents north, 90° represents east, 180° represents south, and 270° represents west. The value identifies the direction from which the wind is blowing. |
| `WSPD` | Wind speed at the 10 m reference measurement height. |
| `WSPD_80` | Wind speed extrapolated from 10 m to an 80 m reference height using a logarithmic wind profile. |

Users applying WAKE-NET to another location should retain the required column names—particularly `WDIR`, `WSPD`, and `WSPD_80`—or update the corresponding column references in `WAKENET.ipynb`.


## Citation:
If you use any of our codes/data for your work, please cite the following papers as your reference:

Ann Mary Toms and Xingpeng Li, “WAKE-NET: A 3D-Wake-Aware Economic Turbine Layout and Cabling Optimization Framework for Multi-Capacity Multi-Hub-Height Wind Farms Serving Grid-Scale and Industrial Power Systems”, *Renewable Energy*, Jun. 2026.

Paper website: https://rpglab.github.io/papers/AnnT-WakeNET/


## Contributions:
Ann Mary Toms developed this set of programs/data. Xingpeng Li supervised this work.


## Contact:
Dr. Xingpeng Li

University of Houston

Email: xli83@central.uh.edu

Website: https://rpglab.github.io/


## License:
This work is licensed under the terms of the <a class="off" href="https://creativecommons.org/licenses/by/4.0/"  target="_blank">Creative Commons Attribution 4.0 (CC BY 4.0) license.</a>


## Disclaimer:
The author doesn’t make any warranty for the accuracy, completeness, or usefulness of any information disclosed; and the author assumes no liability or responsibility for any errors or omissions for the information (data/code/results etc) disclosed.