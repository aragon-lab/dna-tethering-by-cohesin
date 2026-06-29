# Observed residence time
Measures duration that each track in a kympgraph was observed for.  Operates on existing "traces" CSV files, which come from analyses such as[photobleaching-and-stepfinding scripts](../photobleaching-and-stepfinding/).

## Outline
1. Reads "_traces" CSVs from input folder
2. Loads corresponding kymograph TIFF image (for identifying maximum duration)
3. Identifies first and last timepoint for each kymograph to determine observed duration
4. Removes any traces that are present within 5 frames of the end of the kymograph (it is assumed these traces may not have ended)