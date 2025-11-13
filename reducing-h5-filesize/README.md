# Reducing H5 filesize
Removes high frequency force traces from H5 files to reduce overall file size.  Processed files are saved to a mirrored directory structure.  Any non-H5 files are copied as is.

## Requirements
- Pylake, enabled with "-e pylake" flag when launching pixi:
`pixi run -e pylake jupyter lab`

## Outline
1. Recursively scans through folders, identifying H5 files
2. Re-saves files without high frequency traces to mirrored directory structure
3. Reports ongoing file size reduction