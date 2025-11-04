# Tether site intensity analysis
Identifies foci using Laplacian of Gaussian spot detector, then asks user to identify tether point between DNA molecules.  Measures ratio of foci intensity to intensity at tether point.

## Requirements
- [Fiji](https://fiji.sc) and [ModularImageAnalysis (MIA)](https://mianalysis.github.io).  See [guides](https://mianalysis.github.io/guides) page for more information.

## Outline
1. Load kymograph as TIFF image
2. User selects tether point (clicking on tether point, then selecting "Add as new object", then "Finish adding objects")
3. User selects region between beads (drawing round desired region, then "Add as new object" and "Finish adding objects")
4. Foci detection using TrackMate's Laplacian of Gaussian detector
5. Focus closest to user-defined tether point is identified
6. Foci intensities estimated using 2D Gaussian fitting
7. All foci intensities are measured relative to the intensity of the tether point foci