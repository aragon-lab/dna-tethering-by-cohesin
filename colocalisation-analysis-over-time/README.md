# Colocalisation analysis over time
Tracks kymographs, then performs pairwise linking of tracks from two different channels based on their initial positions.  Displacement of each track is calculated relative to its starting position and tracks are visualised as displacement pairs on a 2D plot.

## Requirements
- Noise2Void (N2V), enabled with "-e n2v" flag when launching pixi:
`pixi run -e n2v jupyter lab`

## Outline
1. Loads kymographs from TIFF file
2. (Optionally) Processes image with Noise2Void
3. Tracks kymographs
4. User is asked to specify which tracks to retain for analysis
5. Creates pairwise links between tracks in each channel
6. Calculates displacement of each track relative to initial position.
7. Fits straight line with form y = x + c and extracts R<sup>2</sup>.