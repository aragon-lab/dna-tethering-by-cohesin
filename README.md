# Analysis tools for "Cohesin can tether two DNA molecules without ring entrapment"
Analysis tools used in the publication "Cohesin can tether two DNA molecules without ring entrapment" by Fisher G.L.M, Voulgaris, M., Cross, S.J., Koetje, A.I., Francis, A.J. & Aragon, L.

## 1. Downloading
The easiest way to download the files in this repository is by clicking the green "Code" button above and selecting "Download ZIP".

## 2. Installation
All tools in this repository, with the exception of "tether-site-intensity-analysis" are written in Python using Jupyter notebooks.  Setup information for Jupyter notebooks is shown in [Jupyter notebook setup](#21-jupyter-notebook-setup) and information for "tether-site-intensity-analysis" is provided in [ModularImageAnalysis (MIA) setup](#22-modularimageanalysis-mia-setup).

### 2.1. Jupyter notebook setup
This repository contains pre-configured Python environments using the [Pixi](https://pixi.sh) package manager.  The provided Pixi configuration supports all major platforms: Windows (64-bit), MacOS (64-bit Intel and Apple Silicon) and Linux (64-bit).  To learn more about Pixi, there's an excellent 45 minute [tutorial](https://www.youtube.com/live/ws92c5NFPaU) from the [Jean Golding Institute](https://www.bristol.ac.uk/golding/) (University of Bristol).

To install Pixi, copy and paste the relevant command below into a terminal (e.g. Powershell on Windows or Terminal on MacOS and Linux).  If these commands don't work, please check the latest [Pixi documentation](https://pixi.sh).

- Linux and MacOS: `curl -fsSL https://pixi.sh/install.sh | sh`
- Windows: `powershell -ExecutionPolicy ByPass -c "irm -useb https://pixi.sh/install.ps1 | iex"`

 Once complete, your system should understand the "pixi" command required to run notebooks (see [Launching Jupyter notebooks](#31-launching-jupyter-notebooks)).  The relevant packages (e.g. Jupyter, Numpy, etc.) will be downloaded automatically the first time Jupyter is launched using Pixi.

Note: It's not possible to define a single configuration which is compatible with the dependencies Noise2Void (N2V) and Pylake for Apple Silicon devices (M1, M2, etc.).  These aren't often used in these scripts, so a "default" environment which contains neither exists; however, environments containing either N2V or Pylake have also been provided.

### 2.2. ModularImageAnalysis (MIA) setup
The "tether-site-intensity-analysis" tool uses the [ModularImageAnalysis (MIA)](https://mianalysis.github.io) plugin for ImageJ/Fiji.  To run this, it's recommended to download a new copy of Fiji from [fiji.sc](https://fiji.sc).  Since ImageJ and Fiji are "portable" applications (no installation required), it's not necessary to delete any existing copies.  Once downloaded, the following steps will install MIA:

1. Within Fiji, go to Help > Update...
2. In the "ImageJ Updater" window, click "Manage Update Sites"
3. Put ticks next to the following two update sites:
    - IJPB-plugins
    - ModularImageAnalysis (MIA)
4. Click "Apply and close", then "Apply changes" and restart Fiji when prompted

## 3. Using these tools
### 3.1. Running Jupyter notebooks
1. On Windows, start PowerShell, or on MacOS and Linux, start Terminal
2. If not already there, navigate to the downloaded code folder (it's necessary to be in the folder containing the "pixi.toml" file)
3. Use one of the commands below, depending on whether Noise2Void (N2V), Pylake or neither are required:
    - `pixi run jupyter lab`
    - `pixi run -e n2v jupyter lab`
    - `pixi run -e pylake jupyter lab`

### 3.2. Running ModularImageAnalysis (MIA) workflow
1. Within Fiji, go to Plugins > ModularImageAnalysis (MIA) > MIA
2. Within the MIA interface, click "Load" and select the desired .mia file

Note: Tutorials on using MIA can be found on [YouTube](https://youtube.com/@mianalysis).

## 4. Examples
Each analysis folder contains an "examples" folder, in which there are example inputs and outputs for each analysis