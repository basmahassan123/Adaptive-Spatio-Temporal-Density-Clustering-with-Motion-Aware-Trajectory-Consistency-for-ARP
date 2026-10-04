# AI Application Requirements — Submission Checklist

## 1. Reproducibility
**Addressed.**

`README.md` now includes:
- Title
- Description
- Dataset Information
- Code Information
- Usage Instructions
- Requirements
- Methodology
- Metric definitions
- Citations
- License information
- Contribution guidance

`DATA_AVAILABILITY.md` documents dataset access and explains why the full dataset is not redistributed.

`CONTRIBUTING.md` provides contribution and reproducibility rules.

`LICENSE_NOTICE.md` distinguishes the external RadarScenes dataset license from the current software-license status of the repository.

## 2. Materials & Methods — Computing Infrastructure
The insert-ready manuscript section documents:
- Windows operating system
- Anaconda environment
- Python 3.12.8
- NVIDIA Quadro RTX 3000 Laptop GPU
- 6 GB VRAM
- NumPy, pandas, SciPy, scikit-learn, h5py, HDBSCAN
- Jupyter/IPython notebook environment

The GPU is reported for transparency. The core clustering/evaluation workflow is primarily based on standard scientific-Python routines and does not inherently require a specific GPU.

## Publication note
The current public repository contains `README.md` and `Radar_Final.ipynb`. The full manuscript was not provided in the current task, so `AI_APPLICATION_REQUIREMENTS_MANUSCRIPT_SECTION.docx` is an insert-ready manuscript section rather than a claim that the complete manuscript has been edited.
