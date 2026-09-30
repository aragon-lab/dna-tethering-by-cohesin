# Photobleaching and step-finding
Counting photobleaching steps from kymograph traces.

## Requirements
- Noise2Void (N2V), enabled with "-e n2v" flag when launching pixi:
`pixi run -e n2v jupyter lab`

## Outline
1. Loads kymographs from TIFF
2. Tracks kymographs
3. Measures kymograph intensity at each timepoint
4. Uses implementation of BaLM MATLAB tool to identify photobleaching steps