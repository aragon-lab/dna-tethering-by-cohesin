# Intensity vs force
Measures mean intensity of a kymograph within specified force ranges.  Requires a binarised mask image to denote tether region in each image (suffixed with "_mask").

## Outline
1. Loads kymograph and force data from H5 file
2. Loads corresponding mask TIFF image stored in the same folder, with the suffix "_mask"
3. Measures mean intensity for all kymograph timepoints corresponding to user-specifed force windows
4. Plots intensity vs force for all files in input folder