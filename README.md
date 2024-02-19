# Bioimage-Analysis-Workshop-23-24

The course materials for the bioimage analysis workshop at Kyoto and Taipei. Please note that these materials have been heavily adopted from:

- **EMBL Bio-IT bioimage analysis workshop**, especially the part by Toby Hodges and Jonas Hartmann: [https://git.embl.de/grp-bio-it-workshops/image-analysis-with-python](https://git.embl.de/grp-bio-it-workshops/image-analysis-with-python)
- **Introduction to Bioimage Analysis** by Pete Bankhead: [https://bioimagebook.github.io/](https://bioimagebook.github.io/)
- **Bioimage Analysis Lecture 2020** by Robert Haase: [https://www.youtube.com/watch?v=e-2DbkUwKk4&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U](https://www.youtube.com/watch?v=e-2DbkUwKk4&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U)
- Bioimaging Guide by [Various People](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3002167): https://www.bioimagingguide.org/
- **Bioimage analysis notebook** by Robert Haase: https://haesleinhuepf.github.io/BioImageAnalysisNotebooks

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
    conda install numpy matplotlib scipy scikit-image ipywidgets jupyter jupyterlab pandas 
    ```
    then install [Napari](https://napari.org/stable/) with
    ```powershell
    python -m pip install "napari[all]"
    ```
	for IPMB workshop (Day 2), run this too
    ```powershell
    conda install scikit-learn seaborn umap-learn 
    ```
    ```powershell
    conda install -c conda-forge hdbscan
    ```

4. Launch the Jupyter Lab by
    ```powershell
	jupyter lab
    ```
5. Navigate to the downloaded files

## Past Events

This event was ran four times from Dec 2023 to Jan 2024, they were at:
- Institute of Life and Medical Science (LiMe), Kyoto University, Japan (14-15 Dec)
- Institute of Cell and Organism Biology (ICOB), Academia Sinica, Taiwan (27-28 Dec)
- Institute of Plant and Micro Biology (IPMB), Academia Sinica, Taiwan (9-10 Jan)
- College of Medicine, National Taiwan University (NTUCM), Taiwan (4 & 12 Jan)

The biggest different to the event hosted in the [last year](https://github.com/Koushouu/Bioimage-Analysis-Workshop-Taipei) is that here every event spanned across two days, with day 1 focused on basic Python programming and day 2 on the image analysis. Further more, as oppose to the last time where I just distribute code to everyone then they study the code by themselves, this year I am doing code-along, where I code in the front and explain, and people can follow; then there would be a few code blocks where I ask people to challenge coding for 15 mins ish. 

Also, in the IPMB workshop specifically, all demo images were from the participants; I also included a quick module on dimensional reduction and clustering in BiA in that workshop (The code is available in codelab_ipmb folder).

Additionally, the workshop at LiMe, Kyoto-U was conducted entirely in Japanese - that was a big challenge for myself, but it looks like I made it.

Overall the workshop was successful but there are still many things that could be discussed and improved. For example, about how much to code: most people use imageJ for image analysis and I probably need to rethink the role of coding in image analysis, and why to code. Also, there are many image analysis functionalities that can help the coder to do things in one step, e.g.:
 1) There exists a one line function to delete all ROIs on the edge of a FoV - shall I just use it in code instead of writing a code with for loop to fill ROIs touching the edge to zero? 
 2) ```skimage.measure.regionprops``` can measure many properties of an image/ROI in a line. Shall I still teach people how to extract ROI props by coding the algorithm then run for loop for all ROIs?
 
These are questions that I had in mind over the month that I still couldn't find a conclusion.

Other than this, a few changes I will make to the workshop next year:
1. Choose miniconda + vs-code as the coding environment
2. Having more DL/ML content, but that probably would be an extra day ("an" was too optimistic - maybe)
3. Probably having more short notebooks instead of having two big notebooks (for image analysis) - and include contents on tracking and 3D image analysis, if possible
4. Having more people to run this workshop - if the workshop get longer I will no longer be able to run it on my own. Hopefully two more people to get involved in running this

## Acknowledgment

I thank the Ministry of Education, Taiwan and Cambridge Trust, Queens' College Cambridge for their generous support in providing my PhD funding, opportunity and environment for me to create this workshop.

For each individual workshop:
- Many thanks to 野田岳志先生,中野雅博先生 and 山内康司さん for hosting and supporting the workshop at LiMe, Kyoto-U
- Many thanks to Jung-Kun Wen (IBC ImageCORE) / Wei-Chen Chu (ICOB ImageCORE) for hosting and supporting the workshop at ICOB, AS. Also thanks Zeiss and Olympus for sponsoring the workshop.
- Many thanks to Dr Kimmy Ho and Dr Rachel Wang for hosting and supporting the workshop at IPMB, AS
- Many thanks to Dr Peggy Hsu and members of NTUCM Imaging Core facility for hosting and supporting the workshop at NTUCM
- Also thanks Hsuan-Pei Huang and Yin-Tzu Xie for helping out with workshop at IPMB and NTUCM; Kai-Xiu & Yu-Rong for their assistance at the ICOB workshop
- Finally, many thanks to my family and my girlfriend for their continuous support, ideas and inspirations.

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
