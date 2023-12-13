# Bioimage-Analysis-Workshop-23-24

The course materials for the bioimage analysis workshop at LiMe, KyotoU. Please note that these materials have been heavily adopted from:

- **EMBL Bio-IT bioimage analysis workshop**, especially the part by Toby Hodges and Jonas Hartmann: [https://git.embl.de/grp-bio-it-workshops/image-analysis-with-python](https://git.embl.de/grp-bio-it-workshops/image-analysis-with-python)
- **Introduction to Bioimage Analysis** by Pete Bankhead: [https://bioimagebook.github.io/](https://bioimagebook.github.io/)
- **Bioimage Analysis Lecture 2020** by Robert Haase: [https://www.youtube.com/watch?v=e-2DbkUwKk4&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U](https://www.youtube.com/watch?v=e-2DbkUwKk4&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U)
- Bioimaging Guide by [Various People](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3002167): https://www.bioimagingguide.org/

## Pre-requirement of the workshop

Please prepare the following before the workshop:

- Please install Anaconda ([https://www.anaconda.com/](https://www.anaconda.com/)) on your laptop (Yes, you need a laptop) and follow the “Creating a Python Environment for the workshop” workflow below for the setup.
## Creating a Python Environment for the workshop

1. With the Anaconda prompt, create a virtual environment with the name “bioimage-analysis”

    ```powershell
    conda create --name bioimage-analysis python=3.8
    ```

2. Then activate the environment

    ```powershell
    conda activate bioimage-analysis
    ```

3. Install all the necessary packages

    ```powershell
    conda install numpy matplotlib scipy scikit-image ipywidgets jupyter jupyterlab 
    ```

	then install [Napari](https://napari.org/stable/)with
```powershell
	python -m pip install "napari[all]"
```
4. Launch the Jupyter Lab by
```powershell
	jupyter lab
```
6. Navigate to the downloaded files
