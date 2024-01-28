# Initializing TensorFlow Environment on M3, M3 Pro and M3 Max Macbook Pros.

**TensorFlow on M3, M3 Pro, and M3 Max MacBook Pros: Harnessing Computational Power with Apple Silicon**

**Description**:

Unlock the full potential of your Apple Silicon-powered M3, M3 Pro, and M3 Max MacBook Pros by leveraging TensorFlow, the open-source machine learning framework. This repository is tailored to provide an optimized environment for setting up and running TensorFlow on Apple's cutting-edge M3 chips.

## Key Features:

1. **Efficient ML Workflows:** Streamline your machine learning workflows on Apple Silicon for enhanced efficiency and performance.

2. **Tailored Configurations:** Discover configurations and settings specifically designed for M3, M3 Pro, and M3 Max MacBook Pros, ensuring optimal resource utilization.

3. **Performance Boost:** Leverage the native capabilities of Apple Silicon to achieve accelerated training and inference speeds, tapping into the computational prowess of your M3 MacBook Pro.

4. **Compatibility and Updates:** Stay up-to-date with the latest TensorFlow releases and compatibility updates tailored for Apple Silicon architecture.


**Getting Started:**
Follow all the necessary steps mentioned below.
## Steps
1. Install Homebrew from https://brew.sh.
2. [Download Miniforge3](https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh) for macOS arm64 chips.
3. Install Miniforge3 into the home directory of your Macbook Pro.
4. Type the following Bash code in the terminal.
```bash
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
```
```bash
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
```
```bash
source ~/miniforge3/bin/activate
```
5. Restart terminal to prevent any errors.
6. Create a new directory to setup the custom TensorFlow environment.
```bash
mkdir tensorflow-test
```
```bash
cd tensorflow-test
```
7. Type ls in terminal to crosscheck the current directory.
8. Initialize and activate the Conda environment. 
```bash
conda create --prefix ./env python=3.8
```
```bash
conda activate ./env
```
9. Install TensorFlow dependencies from Apple Conda.
```bash
conda install -c apple tensorflow-deps
```
10. Install base TensorFlow.
```bash
python -m pip install tensorflow-macos
```
11. Install Apple's `tensorflow-metal` to utilize the Apple Metal (Apple's GPU framework) for M3, M3 Pro, M3 Max GPU access.
```bash
python -m pip install tensorflow-metal
```
12. Install data science packages.
```bash
conda install jupyter pandas numpy matplotlib scikit-learn
```
13. Start Jupyter Notebook.
```bash
jupyter notebook
```
14. Type the following code to check TensorFlow version/GPU access.
```python
import numpy as np
import pandas as pd
import sklearn
import tensorflow as tf
import matplotlib.pyplot as plt

# Check for TensorFlow GPU access
print(f"TensorFlow has access to the following devices:\n{tf.config.list_physical_devices()}")

# See TensorFlow version
print(f"TensorFlow version: {tf.__version__}")
```

That's It!!
You should now be able to run all your ML models on Apple's GPU.
Thank You.
