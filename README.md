# Adaptive Spatio-Temporal Density Clustering with Motion-Aware Trajectory Consistency for Automotive Radar Perception

## Description
This repository contains the research implementation associated with the manuscript on Adaptive Spatio-Temporal Density Clustering (Adaptive-STDC) with Motion-Aware Trajectory Consistency for Automotive Radar Perception.

The current repository provides the main experimental implementation as `Radar_Final.ipynb`.

## Dataset Information
The experiments use the RadarScenes dataset, a real-world automotive radar point-cloud dataset recorded using four automotive radar sensors mounted on one measurement vehicle. RadarScenes contains 158 individual sequences, more than four hours of driving data, and point-wise annotations.

The complete dataset is not redistributed in this repository. Obtain it from the official RadarScenes distribution source and comply with its license.

Official resources:
- https://radar-scenes.com/
- https://radar-scenes.com/dataset/about/
- https://zenodo.org/records/4559821
- https://doi.org/10.23919/FUSION49465.2021.9627037

RadarScenes is licensed under CC BY-NC-SA 4.0 according to the official RadarScenes website.

## Code Information
The principal implementation is:
```text
Radar_Final.ipynb
```

The notebook contains data preparation, feature construction, clustering experiments, evaluation, and experimental analysis.

## Usage Instructions
1. Obtain RadarScenes from an official source.
2. Create a Python 3.12 environment, for example:
```bash
conda create -n adaptive_stdc python=3.12
conda activate adaptive_stdc
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```
4. Open `Radar_Final.ipynb` and update its local dataset path.
5. Run the notebook cells in order:
```bash
jupyter notebook
```

Do not commit the full RadarScenes dataset or private workstation paths.

## Requirements
See `requirements.txt` for the principal Python dependencies.

## Methodology
The documented protocol uses:
1. Sequence-level train/validation/test separation.
2. Training-only preprocessing where applicable.
3. Validation-based parameter selection rather than test-set tuning.
4. Controlled random seeds for repeated experiments.
5. The same evaluation protocol for Adaptive-STDC and comparison methods.
6. Spatial, temporal, and motion-related radar features, including compensated Doppler velocity and motion descriptors.
7. Clustering evaluation using Silhouette Score, Davies-Bouldin Index, Calinski-Harabasz Index, Noise Ratio, and Cluster Purity.
8. Frame-wise and chronological temporal processing where applicable.

### Metric definitions
Noise Ratio:
```text
number of noise detections / total evaluated detections
```

Cluster Purity:
```text
sum of dominant ground-truth class counts across predicted non-noise clusters
/ total detections assigned to non-noise clusters
```

## Citations
Schumann, O., Hahn, M., Scheiner, N., Weishaupt, F., Tilly, J. F., Dickmann, J., and Wöhler, C. “RadarScenes: A Real-World Radar Point Cloud Data Set for Automotive Applications.” 2021 IEEE 24th International Conference on Information Fusion (FUSION), 2021. DOI: 10.23919/FUSION49465.2021.9627037.

See `CITATION.md` for citation details.

## License & Contribution Guidelines
The RadarScenes dataset has its own CC BY-NC-SA 4.0 license and is not redistributed here.

This repository currently does not declare a separate software license. Users should not assume an open-source license for the code unless the repository authors explicitly add one.

See `CONTRIBUTING.md` and `LICENSE_NOTICE.md`.
