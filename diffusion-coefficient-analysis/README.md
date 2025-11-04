# Diffusion coefficient analysis
Calculating global and instantaneous diffusion coefficients for kymograph traces

## Requirements
- Noise2Void (N2V), enabled with "-e n2v" flag when launching pixi:
`pixi run -e n2v jupyter lab`

## Outline
1. Loads kymographs from TIFF file
2. (Optionally) Processes image with Noise2Void
3. Tracks kymographs
4. User is asked to specify which tracks to retain for analysis
5. For each track, the global MSD is calculated.  The diffusion coefficient is extracted from the initial gradient of the MSD.
6. For each trace, the instantaneous MSD is calculated and diffusion coefficients calculated at each point.