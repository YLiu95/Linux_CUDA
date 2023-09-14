# CUDA on Linux (WSL) setup notes

## guides

Nvidia guide (CUDA on WSL User Guide)

https://docs.nvidia.com/cuda/wsl-user-guide/index.html#

> NVIDIA CUDA Installation Guide for Linux

https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#wsl

Ubuntu guide (Enabling GPU acceleration on Ubuntu on WSL2 with the NVIDIA CUDA Platform)

https://ubuntu.com/tutorials/enabling-gpu-acceleration-on-ubuntu-on-wsl2-with-the-nvidia-cuda-platform#1-overview

# commands 

launch wsl from cmd: `c:\Windows\system32\wsl`

to user directory: `cd /mnt/c/Users/ISDA`

FXFpML trial run: `autotrain llm --train --project_name FXFpML --model abhishek/llama-2-7b-hf-small-shards --data_path YL95/FXFpML --use_peft --use_int4 --trainer sft --learning_rate 2e-4`

access wsl files in file explorer: `\\wsl$`

## version check in cmd or powershell(admin)

check wsl version: `wsl --list --verbose`

## version check in wsl

check CUDA verison: `nvcc --version`

check Nvidia GPU driver: `nvidia-smi`

check python version: `python3 --version`

check pip version: `pip3 --version`

## sys info

`df -h`: disk usage for all mounted filesystems in a format that's easy to read 
>**Filesystem: /dev/sdc is likely your main WSL filesystem.**

`uname -m && cat /etc/*release`: Get system information

`gcc --version`: Check the GCC compiler version

`uname -r`: Get the kernel version

`ps`: Display currently active processes

`ps -ef`: Display extensive information on all running processes

`df -k`: Display disk usage in kilobytes

`cd /mnt/c/Users/ISDA/Downloads/`: Navigate to a specific directory

`ls -ltr`: List files with additional details

## delete everything on wsl and reinstall wsl

`wsl --terminate Ubuntu`: Terminate Running Instances.

`wsl --unregister Ubuntu`: Uninstall the Distribution

`wsl --list`: Confirm Deletion

`wsl --install`: Reinstall 
