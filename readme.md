# Procedure

```bash
sudo apt-key del 7fa2af80
wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/12.6.1/local_installers/cuda-repo-wsl-ubuntu-12-6-local_12.6.1-1_amd64.deb
sudo dpkg -i cuda-repo-wsl-ubuntu-12-6-local_12.6.1-1_amd64.deb
```

Follow the instruction like below.
```bash
sudo cp /var/cuda-repo-wsl-ubuntu-12-6-local/cuda-*-keyring.gpg /usr/share/keyrings/
```

```bash
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-6
/usr/local/cuda/bin/nvcc --version
```

Install cuDNN.
```bash
sudo apt install zlib1g
sudo dpkg -i /mnt/c/Users/user/Downloads/cudnn-local-repo-ubuntu2204-8.8.1.3_1.0-1_amd64.deb
sudo cp /var/cudnn-local-repo-*/cudnn-local-*-keyring.gpg /usr/share/keyrings/
sudo apt update
sudo apt -y install libcudnn8 libcudnn8-dev libcudnn8-samples
cp -r /usr/src/cudnn_samples_v8/ ~/
cd ~/cudnn_samples_v8/mnistCUDNN/
make clean && make
./mnistCUDNN
```

```bash
sudo apt install -y python3.12 python3.12-venv
```

