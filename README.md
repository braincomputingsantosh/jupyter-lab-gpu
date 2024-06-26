## Quickstart
Ensure that you have access to a computer with an NVIDIA GPU. If you don’t have your own setup, you can try [Saturn Cloud](https://saturncloud.io/) for a free GPU-powered Jupyter solution.

Install Docker version 1.10.0+ and Docker Compose version 1.28.0+.

Get access to your GPU via CUDA drivers within Docker containers. For this, follow the installation steps in this [Medium article](https://medium.com/@christoph.schranz/set-up-your-own-gpu-based-jupyterlab-e0d45fcacf43). You can confirm that you can access your GPU within Docker if the command below returns a result similar to this one:
```
docker run --gpus all nvidia/cuda:12.3.2-cudnn9-runtime-ubuntu22.04 nvidia-smi
```
## jupyterlab-nvdashboard
To run the jupyterlab-nvdashboard extension in JupyterLab, follow these steps:

1. Make sure you have JupyterLab installed. If not, you can install it using pip:

```
pip install jupyterlab
```

2. Install the jupyterlab-nvdashboard extension using pip:

```
pip install jupyterlab-nvdashboard
```

3. Enable the extension in JupyterLab:

```
jupyter labextension install jupyterlab-nvdashboard
```

4. Start JupyterLab:

```
jupyter lab
```

5. In JupyterLab, you should now see a new icon in the left sidebar that looks like a speedometer. Click on this icon to open the nvdashboard.

6. The nvdashboard will display information about your system's GPU usage, including memory usage, GPU utilization, and running processes.

Note: The jupyterlab-nvdashboard extension requires the nvidia-smi command-line utility, which is part of the NVIDIA GPU driver. Make sure you have an NVIDIA GPU and the appropriate driver installed on your system.

If you encounter any issues or need further assistance, refer to the jupyterlab-nvdashboard documentation or seek help from the JupyterLab community.
* https://developer.nvidia.com/blog/gpu-dashboards-in-jupyter-lab/
* https://pypi.org/project/jupyterlab-nvdashboard/

Screenshot:
<img width="1240" alt="image" src="https://github.com/braincomputingsantosh/jupyter-lab-gpu/assets/19161376/ddf8fbaa-ec94-4c2a-bd5e-6cd34e25e6f6">
