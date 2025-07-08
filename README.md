# 2024-jn-omero-pipeline

Material and solutions for the course **"Bioimage data management and analysis with OMERO"**
held in Heidelberg (13th May 2024)

**Module 3 (1.45 pm - 3.45 pm): OMERO and Jupyter Notebooks**

Instructor - Dr Riccardo Massei

### Jupyter Notebook Pipeline Overview

![JN.png](01_presentation%2F01_images%2FJN.png)

Main goal of the workflow is to show the potential of JN to perform reproducible image
analysis in connection with an OMERO instance. In this specific example, we are performing
a simple nuclei segmentation from raw images uploaded in OMERO. 

Overview on the JN pipeline:
1) **Connect to OMERO using the python API**
2) **Fetch an image for image analysis**
3)  **Perform the following pre and post-processing steps**

   3a) Denoising
   3b) Binarization 
   3c) Labelling 
   3d) Feature extraction
4) **Push Results back to OMERO by adding metadata and additional informations**

Furthermore, it will be show how to process can be automatized by the execution of
automatic loops throught the OMERO datase. Most of the pre and post-processing step 
were created by taking inspiration from the [Bio-image Analysis Notebooks](https://haesleinhuepf.github.io/BioImageAnalysisNotebooks/intro.html).
We thanks Robert Haase for creating this material.

## Course Preparation and checklist

----

### Connect to the OMERO instance

You can 1) connect to your institutional instance, 2) [run OMERO.server and OMERO.web using docker-compose](https://github.com/ome/docker-example-omero) locally or 3) 
use temporary OMERO account prepare by Müster University which can be accessed and used the day of the course. 
More information regarding these accounts will be give the day of the course. 

### IMPORTANT - Installing ezomero
Please, follow the instruction on the [ezomero GitHub repository](https://github.com/TheJacksonLaboratory/ezomero) to install ezomero.
All other libraries can be found in requirements.txt

### Run the Jupyter Notebook
Jupyter is open-source software and service for interactive computing.

We suggest to install the conda environment before the course and
run JN locally on your personal computer.

Optionally, you can also use the service **GoogleColab**. Please, install your conda environment with omero-py writing the following command (in case of Python 3.10):

````
 pip install https://github.com/glencoesoftware/zeroc-ice-py-linux-x86_64/releases/download/20240202/zeroc_ice-3.6.5-cp310-cp310-manylinux_2_28_x86_64.whl 
 pip install ezomero
````

### Examplary dataset for the present course...

We used image set BBBC014v1 provided by Ilya Ravkin, available from the Broad Bioimage Benchmark Collection [Ljosa et al., Nature Methods, 2012].
For details and biological 
background see https://www.broadinstitute.org/bbbc/BBBC014/. Images can be founded in this repository at
01_data/HCS_data.zip.
**Data need to uploaded into your OMERO instance before the exercise. Otherwise, data will
be already uploaded in the prepared server**

#### ..or bring your own data :)
In case you have your own data and want to perform a basic nuclei segmentation, your 
dataset is welcome. In case, you can also browse [IDR](https://idr.openmicroscopy.org/) for potential and interesting case studies.

### Useful resources before the course:

- **Jupyter Notebook Webpage**:

https://jupyter.org/

- **OMERO Python API**:

https://docs.openmicroscopy.org/omero/5.6.0/developers/Python.html

- **Bio-image Analysis Notebooks**:

https://haesleinhuepf.github.io/BioImageAnalysisNotebooks/intro.html

https://scikit-image.org/