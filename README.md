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
automatic loops throught the OMERO datase.

## Course Preparation and checklist

----

### Connect to the OMERO instance

You can 1) connect to your institutional instance, 2) [run OMERO.server and OMERO.web using docker-compose](https://github.com/ome/docker-example-omero) locally or 3) 
use temporary OMERO account prepare by Müster University which can be accessed and used the day of the course. 
More information regarding these accounts will be give the day of the course. 

### Run the Jupyter Notebook
Jupyter is open-source software and service for interactive computing.

We suggest to install the conda environment before the course and
run JN locally on your personal computer. However, there is also the option to 
run the JN on the 
[**Helmholtz Cloud Service**](https://helmholtz.cloud/services/?serviceDetails=jupyter-desy&serviceID=955f806d-9936-4fa2-993b-e0e1abd483db):

- The DESY hosted [Jupyter service](https://jupyter.desy.de/hub/login) allows users to start JupyterLab notebooks. 
On request, users can include additional Jupyter Server environments as Docker images.

However, we cannot promise that the service will be working the day of the course.



### Setup the conda environment
- You can set-up your environment using the **py_pipeline.yml** **_before the course_**. In case of problems, please contact the organizators.


### Examplary dataset for the present course...

Exercise data are part of the SBS Bioimage CNT image set provided by Ilya Ravkin and 
available from the Broad Bioimage Benchmark Collection. For details and biological 
background see https://www.broadinstitute.org/bbbc/BBBC014/. Images can be downloaded at 
this [link](https://data.broadinstitute.org/bbbc/BBBC014/BBBC014_v1_images.zip). 
**Data need to uploaded into your OMERO instance before the exercise.**

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
