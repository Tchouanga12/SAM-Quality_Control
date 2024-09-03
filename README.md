# SAM-Quality_Control

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/Tchouanga12/SAM-Quality_Control/blob/main/LICENSE)
[![Python version](https://img.shields.io/badge/python-3.7%2B-brightgreen.svg)](https://www.python.org/downloads/)
[![Contributors](https://img.shields.io/github/contributors/Tchouanga12/SAM-Quality_Control.svg)](https://github.com/Tchouanga12/SAM-Quality_Control/graphs/contributors)

**SAM Quality Control** is a Python-based project designed to automate and enhance quality control processes for manufacturing or service environments. The tool provides a robust framework for monitoring, analyzing, and reporting on quality metrics, ensuring that standards are consistently met.

## Use Case
Solving the problem of void detection on electronic components using SAM (Segment Anything Model)

Given an input image or a batch of input images, our app can:
- Detect electronic components and voids (small, empty spaces or gaps that can form within materials used in the construction of electronic components)
- Segment electronic components and voids
- Print a segmentation report with several metrics such as the component area and the percentage of area occupied by void.

Directory Structure
Here's a brief overview of the project's directory structure:

data/
    └── Contains our data files (images).

Data_Transformation/
    ├── train/           # Training data files.
    ├── test/            # Testing data files.
    ├── validation/      # Validation data files.
    └── data.yaml        # Configuration file for data processing.

PCB_xray_dataset/
    └── Contains the raw data.

model/
    ├── YOLO/            # YOLO detection models.
    └── SAM/             # SAM segmentation models.
    # Models are ready to be used.


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
