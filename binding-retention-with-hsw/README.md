# Binding retention with high salt wash (HSW)
Uses user-defined regions of interest to measure the percentage of fluorescence remaining after moving protein-bound tether into a high salt channel.

## Requirements
- [Fiji](https://fiji.sc) and [ModularImageAnalysis (MIA)](https://mianalysis.github.io).  See [guides](https://mianalysis.github.io/guides) page for more information.

## Outline
1. Load kymograph as TIFF image.
2. User selects region of interest (ROI) in imaging channel just prior to moving to high salt channel.
3. User selects ROI in imaging channel as soon as motion to high salt channel has begun (i.e. when tether is pulled out of confocal volume).  This is a background reference for normal salt conditions.
4. User selects ROI in high salt channel just prior to motion stopping.  This is a background reference.
5. User selects ROI in high salt channel just after motion stops (i.e. when tether has returned to confocal volume).
6. Mean fluorescence intensity if measured for the four ROIs.
7. The background in normal and high salt conditions are subtracted, using the relevant references.
8. ROIs are drawn on image and saved to file with suffix "_regions".
9. ROIs are saved to .zip files, so they can be easily reused or edited.
9. The intensity ratio of high salt to normal salt is recorded and exported for each image to Excel file.