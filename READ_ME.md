* * *
* * *
# CALIBRATION FOR THERMO NITON XL5 PLUS
* * *
* * *
## E. ANTTILA, UC SANTA BARBARA, eanttila@ucsb.edu
* * *

This folder contains scripts and data to correct raw unknown measurements analyzed with our Thermo Niton XL5 Plus handheld XRF (pXRF).

NITONXL5_StandardCorrelationNEW.ipynb is a Jupyter notebook that generates a calibration model for all elements measured by the pXRF by comparing known and measured elemental abundances in several standards.
This notebook outputs a .csv with all data used to apply the calibration correction to unknown data, as well as figures depicting the calibration model for each element.

ApplyXRFCorr.ipynb is a Jupyter notebook that takes these calibration models and applies them to raw data output from the pXRF, generating a .csv with corrected data.

* * *
## WORKFLOW FOR CORRECTING RAW DATA:

1. Save uncorrected data file (the .csv output by the pXRF and downloaded using NitonConnect) to the directory /INPUT_CSV/Pre-Correction Data/
2. Open ApplyXRFCorr.ipynb, and run each cell consecutively. Make sure to import the correct new data file, and change output data file names accordingly.
3. Output data file, which includes sample names and corrected elemental abundances and uncertainties for each element, is by default saved to OUTPUT_CSV/Corrected_Data/

* * *
## WORKFLOW FOR ADDING NEW STANDARD DATA:

1. For each new XRF run, save all standards in a new tab the Standards_Compiled.xlsx spreadsheet, found in the shared Drive folder in the Standard Data directory.
2. Copy and paste newly collected standard data into the requisite .csv found in /Calibration/INPUT_CSV/Standard Data/{StandardNAME}NEW.csv
### IMPORTANT: MAKE SURE NAME (SAMPLE DEPTH), ELEMENT, AND UNCERTAINTY COLUMNS OF NEW DATA ALIGN WITH PROPER COLUMNS!!!!!
3. Open and run all cells of NITONXL5_StandardCorrelationNEW.ipynb. This generates new calibration schemes for all elements using all standard data, including what you've just added.
4. Profit?

* * *
### IMPORTANT: IF YOU WANT TO ADD ADDITIONAL STANDARDS TO CALIBRATION SCHEME, EACH MUST BE ADDED TO THE NITONXL5_StandardCorrelationNEW.ipynb NOTEBOOK, FOLLOWING FORMATTING FOR EXISTING STANDARDS. 
* * *
