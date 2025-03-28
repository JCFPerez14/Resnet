# 🧠 Deep Learning Training Guide

This repository is designed to help you set up your environment for running deep learning models, especially with TensorFlow and GPU support on Windows (NVIDIA GPU).

---

## ✅ Requirements

- Anaconda or Miniconda (Download from [Anaconda](https://www.anaconda.com/download/success))
- NVIDIA GPU (Optional, for acceleration)
- VS Code (Recommended for running Notebooks)

## Installing the cuda for windows

- cuda-11.2 (https://developer.nvidia.com/cuda-11.2.0-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal)
- cudnn-8.1 (https://developer.nvidia.com/rdp/cudnn-archive)
- install cuda 11.2
- unzip the cudnn
- make a folder in C drive called "Tools" or what ever you want to call it
- open start and search for "Edit the system environment variables"
- Next go to "Environment Variables" then go to "System variables"
- Next add the new variables as shown below change "Tools" if needed
- C:\Tools\cuda8\bin
- C:\Tools\cuda8\include
- C:\Tools\cuda8\lib\x64

---

## 🛠️ Setup Instructions

### 1. Install Anaconda / Miniconda

👉 Download and install from [https://www.anaconda.com/download/success](https://www.anaconda.com/download/success)

---

### 2. Create a Virtual Environment

Open **Anaconda Prompt** and run:

```bash
conda create -n your_env_name python=3.10 anaconda
```

### 3. Activate the Environment

```bash
conda activate your_env_name
```

### 4. Install TensorFlow (Choose based on your setup)

💻 With NVIDIA GPU Support (Recommended):

```bash
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
python -m pip install "tensorflow<2.11"
```

💻 Without GPU Support:

```bash
python -m pip install "tensorflow<2.11"
```

### 5. Install Project Dependencies

📜 Option 1: If you're in the project directory:

```bash
pip install -r requirements.txt
```

📂 Option 2: Specify the path to requirements.txt

```bash
pip install -r path/to/your/requirements.txt
```

📦 Option 3: Manually install the required packages using pip.

### 6. Install Visual Studio Code (VS Code)

👉 Download from https://code.visualstudio.com/
✅ Install the Jupyter Notebook extension from the VS Code extensions marketplace.

### 7. Load the Training Notebook

Open your `.ipynb` file in VS Code.

### 8. Select the Correct Kernel

On the top right, click `"Select Kernel"`
Choose your Anaconda environment (the one you created earlier).

### 9. ✅ Train your Model!

Run the cells and start training 🚀

### Check for cuda

- pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
- gpu-test.ipynb

### 📌 Notes

TensorFlow 2.11 and above drops GPU support for native Windows. That's why we use `tensorflow<2.11`.
Make sure your NVIDIA GPU drivers and CUDA are properly set up if running with GPU.
