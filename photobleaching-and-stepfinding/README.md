# Photobleaching and step-finding
Counting photobleaching steps from kymograph traces.

## Requirements
- Pylake, enabled with "-e pylake" flag when launching pixi:
`pixi run -e pylake jupyter lab`

## Outline
1. Loads kymographs from either TIFF or H5 (BlueLake) file
2. Tracks kymographs
3. Measures kymograph intensity at each timepoint
4. Uses implementation of BaLM MATLAB tool to identify photobleaching steps