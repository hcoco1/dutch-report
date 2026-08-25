# Appendices

## Appendix A — Data dictionary

Description of the fields in the final analytical dataset.

## Appendix B — Data processing

Summary of the data-processing workflow and scripts.

## Appendix C — Validation

Data-quality checks and validation results.

## Appendix D — Additional maps

Supporting maps not included in the main report.

## Appendix E — Reproducibility

Python environment, package versions, repository structure, and instructions for reproducing the analysis.


``` python title="catchments.py"
import geopandas as gpd

stations = gpd.read_file("stations.gpkg").to_crs(28992)
```
``` bash linenums="1"
python -m venv .venv
source .venv/bin/activate
pip install geopandas shapely
```

``` python linenums="1"
buffers = stations.to_crs(28992).buffer(1000)
```