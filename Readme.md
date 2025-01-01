# DTMF Signal Generation and Noise Addition

This repository contains Python code for generating Dual-tone Multi-frequency (DTMF) signals and adding Gaussian noise to simulate real-world conditions. DTMF signals are used in telecommunication systems, where each key on a keypad is represented by a combination of two sine waves (one from a low-frequency group and one from a high-frequency group).

## Requirements

- Python 3.x
- Libraries:
  - numpy
  - matplotlib
  - pandas
  - tensorflow

To install the required libraries, you can use the following pip commands:

```bash
pip install numpy matplotlib pandas tensorflow
```

## Features

__DTMF Signal Generation__: The code generates DTMF signals for each key on a standard 12-key keypad, which includes keys 1-9, 0, '*' and '#'.

__DTMF Signal Visualization__: The signals are visualized using matplotlib to create a clear representation of the waveforms for each key.

__Noise Addition__: Gaussian noise is added to each generated signal to simulate real-world noise in the system. The noise is generated with a standard deviation of 2,4,6 and lastly anywhere in range (2,6) to each signal multiple times.

__Data Storage__: The clean and noisy signals are stored as dataframes for easy further analysis or processing.

## Code Overview

__DTMF Signal Generation__: The low-frequency and high-frequency components for each key are combined to create the corresponding DTMF signal. For example, the key "1" is represented by the combination of 697 Hz and 1209 Hz sine waves.

**Noise Addition**: A function add_noise is defined that adds Gaussian noise to a signal. This noise is added to each DTMF signal 200 times for every key, generating noisy datasets.

**Deep Neural Network**: Later we use a DNN to predict the signals in presence of noise.