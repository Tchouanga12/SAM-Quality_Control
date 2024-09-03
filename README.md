# SAM-Quality_Control

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/Tchouanga12/SAM-Quality_Control/blob/main/LICENSE)
[![Python version](https://img.shields.io/badge/python-3.7%2B-brightgreen.svg)](https://www.python.org/downloads/)
[![Contributors](https://img.shields.io/github/contributors/Tchouanga12/SAM-Quality_Control.svg)](https://github.com/Tchouanga12/SAM-Quality_Control/graphs/contributors)

**SAM Quality Control** is a Python-based project designed to automate and enhance quality control processes for manufacturing or service environments. The tool provides a robust framework for monitoring, analyzing, and reporting on quality metrics, ensuring that standards are consistently met.

## Use Case
Solving the problem of void detection on electronical components using SAM (Segment Anything Model)

Given an input image or a batch of input images, our app is able to:
- **detect** *electonical components* and *voids*;
- **segment** *electonical components* and *voids*;
- print a *segmentation report* with several metrics such as the component area and the percentage of area occupied by void.

# Project Architecture

- **data**: A directory contaning our data files (images).
    - **Data_Transformation**: Contains the train, test, and validation data, as well as the data.yaml file.
    - **PCB_xray_dataset**: Contains the raw data.

- **model**: this directory contains our YOLO detection and SAM segmentation models. They're ready to be used.

- **templates**: Contains the basic HTML code we need to run our app.
    - **base.html**: The base architecture with free slots waiting to be filled with some content
    - **index.html**: Our app entry point, extending `base.html`.

- **app.py**: where are defined the route functions of our app.

- **detection.py**: contains the YOLO detection script.

- **segmentation.py**: contains the SAM segmentation script.

- **report.py**: contains the report generation script.

- **all.py**: contains script that runs all the three operations.
