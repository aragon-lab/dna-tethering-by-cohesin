# Colocalisation analysis single timepoint
Detects peaks in a single timepoint scan and calculates distance to closest peak in opposite channel.

## Outline
1. Loads 2D scan from TIFF file
2. Creates single 1D trace for each channel from the average of multiple rows
3. Detects peaks in single traces
4. Links closest peaks in each channel