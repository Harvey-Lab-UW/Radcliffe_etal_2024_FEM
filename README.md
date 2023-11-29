# Radcliffe_etal_2024_FEM

This is the latest release of data for reproducing the analyses in the manuscript 'How are long-term stand structure, fuel profiles, and potential fire behavior affected by fuel treatment type and intensity in Interior Pacific Northwest forests?' by Radcliffe, Bakker, Churchill, Alvarado, Peterson, Laughlin, and Harvey, published in *Forest Ecology and Management*. See the main text of the manuscript for complete description of data collection and analyses.

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg 

Any user of these data ("User" hereafter) is required to cite it appropriately in any publication that results from its use. These data may be actively used by others for ongoing research, so coordination may be necessary to prevent duplicate 
publication. The User is urged to contact the authors of these data for questions about methodology or results. The User is encouraged to consider collaboration or co-authorship withauthors where appropriate. Misinterpretation of data may occur if used out of context of the original study. Substantial efforts are made to ensure accuracy of the data and documentation, however complete accuracy of data sets cannot be guaranteed. All data are made available as is. Data may be updated periodically and it is the responsibility of the User to check for new versions of the data. The authors and the repository where these data were obtained shall not be liable for damages resulting from any use or misinterpretation of the data.

There are 3 main data files made available for reproducibility purposes:

* plot_level_data.csv
* tree_level_data.csv
* treatment_and_unit.csv


**plot_level_data.csv**

This file contains information aggregated at the plot-level, including predictor variables, field-measured response variables, and modelled response variables.  These data are presented in 'long' format for easy processing with Tidyverse functions in R.  The following columns are included:

* **plot**: unique identifier for plot, presented as unit_number.
* **period**: period of data collection: pre-treatment (2000-2001), and long-term (2019-2020, 13-18 years after treatment).
* **variable**: variable represented.  See publication and plot_level_metadata.csv for more information on individual variables.
* **value**: measured value of the variable.  See publication and plot_level_metadata.csv for more information on individual variables. 
* **variable_type**: predictor, response_field_measured, or response_modelled.


**tree_level_data.csv**

This file contains information aggregated at the individual tree-level for live trees only, necessary for modelling tree mortality and canopy fuel.  To intuitively preserve information at the individual tree level, this file is somewhat 'wider' than the plot_level_data.csv.  The following columns are included:

* **plot**: unique identifier for plot, presented as unit_number.
* **plot_size**: area, in square meters, of the plot in which trees were measured.
* **period**: period of data collection: pre-treatment (2000-2001), and long-term (2019-2020, 13-18 years after treatment).
* **species**: species of individual tree; pipo = *Pinus ponderosa*, psme = *Pseudotsuga menziesii*, abgr = *Abies grandis*, laoc = *Larix occidentalis*.
* **dbh**: diameter at breast height, in centimeters, measured using standard protocols.
* **height_to_live_crown**: lowest height where continuous live canopy begins on a tree, in meters.
* **total_height**: total height of the tree, in meters.


**treatment_and_unit.csv**

This file gives the experimental unit name and treatment type for each of the 204 plots used in analysis. 

* **plot**: unique identifier for plot, presented as unit_number.
* **unit**: name of the experimental unit in which the plot was located.  There are 8 distinct experimental units.
* **treatment**: treatment type applied to plot.  Includes control, burn, thin, and thin plus burn units.  See publication for more information.


In addition, there is one metadata files included to provide additional context:
* **plot_level_variable_metadata.csv**: provides information on units and collection of variables, to contextualize the 'variable' and 'value' columns in the plot_level_data.csv file.
