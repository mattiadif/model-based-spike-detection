[![File Exchange](https://camo.githubusercontent.com/823517a308abad3fee54b061cea8cbc4b70cc41fa731602e64f2e80d01ffcd85/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f46696c6525323045786368616e67652d4d617468576f726b732d6f72616e6765)](https://it.mathworks.com/matlabcentral/fileexchange/162101-model-based-spike-detection)
![MATLAB/Simulink](https://img.shields.io/badge/Matlab%2FSimulink-BF4806.svg?style=flat-square&logo=matlab&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)

[![](https://github.com/MattiaDif/model-based-spike-detection/raw/main/img/spike-detection.png?raw=true)](https://github.com/MattiaDif/model-based-spike-detection/blob/main/img/spike-detection.png?raw=true)

# Model-based online implementation of spike detection algorithms for neuroengineering applications

Neural spike detection algorithms developed in Simulink®.

With this repo you can test and compare different spike detection models implemented in Simulink to simulate real-time signal processing, or to evaluate the performance of a suite spike detection algorithms. Test recordings are available so that you can try the repo functionalities.

[![](https://github.com/MattiaDif/model-based-spike-detection/raw/main/img/models.png?raw=true)](https://github.com/MattiaDif/model-based-spike-detection/blob/main/img/models.png?raw=true)

**Fig.1 - Spike detection models currently developed at the current state of the project**

[![](https://github.com/MattiaDif/model-based-spike-detection/raw/main/img/SNEO.png?raw=true)](https://github.com/MattiaDif/model-based-spike-detection/blob/main/img/SNEO.png?raw=true)

**Fig.2 - SNEO Simulink model**

## Required Software

1. MATLAB® and Simulink® version R2020a or later
2. Signal Processing Toolbox

## Installation

To clone this repo open your terminal and run:

`git clone https://github.com/MattiaDif/model-based-spike-detection.git`

Rember to add the repo to the Matlab path!

## Quick Start

1. Clone the repo and add it to your MATLAB path (see Installation above).
2. Open `Spike_Detection_models/SingleChannelModels` (or `MultiChannelModels` for multi-channel) in MATLAB.
3. Pick a model category and run its `..._run.m` script (e.g. a file prefixed `float_sch_run` for single-channel): this configures the model parameters and launches the Simulink simulation using the bundled `TestData`.
4. To generate your own simulated recordings instead of using the bundled test data, see the `Recording_Generator` folder below.

## Repo description

Inside Spike_Detection_Models:

1. SingleChannelModels: folder that contains the Simulink model for spike detection in single-channel modality subdivided by category. The files named with the prefix float_sch are the spike detection Simulink models, while the files named with the prefix float_sch_run are the Matlab scripts to control the model parameters and lunch the simulation.

2. MultiChannelModels: folder that contains the Simulink model for spike detection in mutli-channel modality subdivided by category. The files named with the prefix float_mch are the spike detection Simulink models, while the files named with the prefix float_mch_run are the Matlab scripts to control the model parameters and lunch the simulation.

3. TestData: folder that contains data for testing the model in Simulink (see the readme.txt file in the folder for further details).

4. Recording_Generator: folder that contains Python scripts to generate simulated multichannel recording exploting MEArec ([MEArec repo](https://github.com/alejoe91/MEArec.git)). This has a separate Python dependency (MEArec) from the MATLAB/Simulink side of the repo — see the MEArec repo for its own installation instructions.

## Background

Different spike detection models have been developed in Simulink to investigate their feasibility in a real-time environment. The algorithms are subdivided among 3 main categories according to the spike detection methods found in literature:

1. Sample Thresholding: a spike is detected if the sample overcomes a threshold or a combination of thresholds.
2. Energy Operator: non-linear energy operator (NEO) computation to enhance the high frequency content of the signal. A spike is detected if the NEO sample overcomes a threshold.
3. Template Matching: spike detection based on the similarity between a waveform and a template. A spike is detected if the similarity metric is greater than a set value.

## DOCUMENTATION

You can find detailed documentation here: [docs](https://mattia-di-florio.gitbook.io/model-based-spike-detection/).

## CORE TEAM

The following people have contributed to the current state of the project. Specifically:

- Development: [Stefano Buccelli](https://www.iit.it/it/people-details/-/people/stefano-buccelli) [1], [Mattia Di Florio](https://rubrica.unige.it/personale/UUZFUllo) [1],[3].
- Conceptualization/Supervision: [Vijay Iyer](https://www.mathworks.com/matlabcentral/profile/authors/6910229) [2], [Akshay Rajhans](https://www.mathworks.com/matlabcentral/profile/authors/4409783) [2], [Stefano Buccelli](https://www.iit.it/it/people-details/-/people/stefano-buccelli) [1], [Michela Chiappalone](https://rubrica.unige.it/personale/UkNHWlNg) [1],[3].

For any questions, please reach via email Mattia Di Florio (di.florio.mattia@gmail.com) or Stefano Buccelli (stefano.buccelli@iit.it) or write an issue!

1. Rehab Technologies IIT-INAIL Lab, Istituto Italiano di Tecnologia, Via Morego 30, 12 16163 Genova, Italy
2. MathWorks, 1 Lakeside Campus Drive, Natick, MA 01760, USA
3. Department of Informatics, Bioengineering, Robotics, System Engineering (DIBRIS), 20 University of Genova, Via all'Opera Pia 13, 16145, Genova, Italy

## REFERENCE

For further information please refer to the scientific publication: [link](https://doi.org/10.1109/EMBC48229.2022.9871444).

If you use this repo, please cite:

"Di Florio, M., Iyer, V., Rajhans, A., Buccelli, S., & Chiappalone, M. (2022, July). Model-based online implementation of spike detection algorithms for neuroengineering applications. In 2022 44th Annual International Conference of the IEEE Engineering in Medicine & Biology Society (EMBC) (pp. 736-739). IEEE."
