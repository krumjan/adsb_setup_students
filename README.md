OSN ADS-B Setup
==============
This repositry contains instructions for students doing a PA, BA, VT or MT involving ADS-B data at the ZAV. This includes step-by-step instruction on how to set up an appropriate python-installation as well as some tutorials on how to work with the Traffic python library.


is intended to serve as an instruction on how to get a setup suited to work with ADS-B data for students  set up all the elements required to work with ADS-B data for PA, BA, VT and MT 

## 1. Setup of Miniconda
In a first step it is necessary to get a recent Python installation on your computer. The latest version of Miniconda can be installed from this [Website](https://docs.conda.io/projects/miniconda/en/latest/). 

## 2. Setup of VSCode
In a next step it is necessary to download and install a programming environment. While it is possible to use any Programming environment that supports Python, it is highly recommended to use VSCode which can be downloaded from this 
[Website](https://code.visualstudio.com/Download).

## 3. Setup of Poetry
In VSCode open a Terminal and enter the following line in the Terminal 

```bash
conda install -c conda-forge poetry
```
- Poetry setup
    - conda install -c conda-forge poetry
    - poetry config virtualenvs.in-project true
    - poetry init → add (numpy, pandas, traffic)
    - poetry install

## 4. Enter OSN Credentials
To fetch data from the OpenSky Network using the Traffic library, it is necessary to provide Traffic with your acces credentials. This is done by entering them in a config file of the library. To locate the file on your computer, open any notebook and enter the following two lines and exectue them:
```python
import traffic
traffic.config_file
```
This should output the path to the traffic.conf file. Open this file with any text editor and locate the part that looks as shown below.

```
[opensky]
username =
password =
```
Enter your OSN username and password and save the edited file.

---
