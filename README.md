# no2-o3-calibration

This notebook captures preliminary remote NO2/O3 calibration results for the 
Breathe Providence network. This remote calibration technique is based on work
completed by Winters et al. (*).

Breathe Providence maintains 25 low cost BEACO2N air sensors throughout the
city. Providence as a city lacks a dense network of government run reference
grade air sensors that are utilized in remote calibration techniques. Only a
single DEM run reference site capable of measuring NO2 is present outside 
(and "upwind") of Providence. To circumvent this, we utilize a network of
QuantAQ MODULAIR sensors that are equipped with labratory based backend
calibrations. These four Modulairs are collocated with BEACO2N sensors 
throughout the city and provide the reference time series of O3/NO2 that the
sensors are calibrated against.

Note that ozone is not yet included in calibrations. The only approach included
thus far is using three of the four MODULAIRs that are located within the city
and excluding the MODULAIR at the Myron J. Francis Site. Some other approaches
have code started but not completed.

The general order to the run the files are:

data cleaning.ipynb -> forming datasets and EDA.ipynb -> 
no2_low_RSD_analysis.ipynb -> forming ML ready no2 datasets.ipynb ->
forming NC ML ready no2 datasets.ipynb -> no2 dpp models.ipynb -> 
no2 NC dpp models.ipynb

(*) (Winter, Anna R., et al. “A Scalable Calibration Method for Enhanced
Accuracy in Dense Air Quality Monitoring Networks.” Environmental Science &amp;
Technology, vol. 59, no. 5, 28 Jan. 2025, pp. 2599–2610,
doi:10.1021/acs.est.4c08855. )