## TensorFlow gpu setup
### Install CUDA dependancy 

~~~
sudo apt-get update  
sudo apt-get install build-essential dkms  
sudo apt-get install freeglut3 freeglut3-dev libxi-dev libxmu-dev  
~~~

### Download and install CUDA 10.1
- 10.1 기준
- Ubuntu 18.04, x86-64, deb[network]
- 다운로드 된 디렉토리에서 터미널 실행
~~~
sudo dpkg -i cuda-repo-ubuntu1810_10.1.105-1_amd64.deb
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1810/x86_64/7fa2af80.pub
sudo apt-get update
sudo apt-get install cuda
~~~

# Install NVIDIA driver
~~~
sudo apt-get install --no-install-recommends nvidia-driver-418
~~~

#Reboot
~~~
sudo reboot
~~~

# Environment Variable Configuration
~~~
sudo vim ~/.bashrc
~~~
- .bashrc 파일에 추가
~~~
export CUDA_HOME=/usr/local/cuda
export LD_LIBRARY_PATH=${CUDA_HOME}/lib64
PATH=${CUDA_HOME}/bin:${PATH} 
export PATH 
~~~

# download and install cuDNN
- CUDA 10.1, ubuntu 18.04
[cuDNN download](https://developer.nvidia.com/rdp/cudnn-download#a-collapse765-10)

