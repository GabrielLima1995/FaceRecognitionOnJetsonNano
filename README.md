# Face Recognition Library for Jetson Nano

This repository provides pre-built wheel files for the `face_recognition` library for the Jetson Nano platform. These wheels can be installed easily on a Jetson Nano to enable face recognition capabilities without the need for building from source.

[For more information about the library](https://pypi.org/project/face-recognition/)

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Creating a Virtual env](#creating-a-virtual-env)
  - [Upgrading PIP and Installing Other Packages](#Upgrading-pip-and-installing-other-packages)
  - [Installing from Wheels](#installing-from-wheels)
  - [Installing Face Recognition Library](#installing-face-recognition-library)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The `face_recognition` library is a simple and powerful library built of `dlib` for detecting and recognizing faces in images. Due to the Jetson Nano's architecture, compiling `dlib` and `face_recognition` from source can be challenging and time-consuming. This repository provides ready-to-install wheel files to simplify this process.

## Installation

### Prerequisites
Before installing the wheels, ensure that your Jetson Nano has the following dependencies:

1. **JetPack SDK** is installed and configured.
2. **Python 3.8+** installed.
3. **dlib** library dependencies:
   - `python3-pip`
   - `libjpeg-dev`
   - `cmake`
   - `libopenblas-dev`
   - `liblapack-dev`
   - `build-essential`
   - `libgtk-3-dev`



Run the following commands to install these dependencies:

```bash
sudo apt update
sudo apt-get install python3-pip cmake libopenblas-dev liblapack-dev libjpeg-dev build-essential libgtk-3-dev
```

### Creating a Virtual Env

After that, create a virtual env and activate it: 

```bash 

python3.8 -m venv face_venv 
source face_venv/bin/activate
```

### Upgrading PIP and Installing Other Packages: 

Install the following packages :

``` bash 

pip install --upgrade pip setuptools wheel
pip install numpy
pip install pillow
pip install opencv-python==4.10.0.84
```

### Installing from Wheels:

``` bash
git clone
pip install dlib-19.24.6-cp38-cp38-linux_aarch64.whl 
pip install face_recognition_models-0.3.0-py2.py3-none-any.whl
```
### Installing Face Recognition Library:

``` bash
pip install face_recognition
```

## Usage

Once installed, the face_recognition library can be used for face detection and recognition in your Jetson Nano-based projects. For example, to recognize faces in an image:

``` python
import face_recognition
```

## Contributing 

If you encounter any issues or have suggestions to improve this repository, feel free to open an issue or submit a pull request.

## Licenses

This project is licensed under the MIT License.
