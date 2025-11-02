# Foci counting
Detects peaks in a single timepoint scan and reports the number of detected foci and their fitting parameters

## Outline
1. Loads 2D scan from TIFF file
2. Creates single 1D trace for each channel from the average of multiple rows
3. Detects peaks in single trace