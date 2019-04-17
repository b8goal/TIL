# CUDA 설치하기
- 현재 CUDA 최신 버전은 9.1이지만 TensorFlow는 CUDA 8.0 설치를 요구하고 있습니다. 따라서 여기에서도 CUDA 8.0을 설치하겠습니다.
- CUDA 8.0 다운로드 페이지 (https://developer.nvidia.com/cuda-80-ga2-download-archive)에 들어갑니다.
- Linux > x86_64 > Ubuntu > 16.04 > deb (local)을 선택하고 다운로드합니다.
- 다운로드 페이지에서 안내되는 것처럼 다음 명령어를 입력합니다.
```
sudo dpkg -i cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb
sudo apt-get update
sudo apt-get install cuda
sudo reboot
```
- bashrc 파일을 열고 맨 아래에 다음 환경변수를 추가합니다.
```
gedit ~/.bashrc

export CUDA_HOME=/usr/local/cuda-8.0
export PATH=/usr/local/cuda-8.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-8.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```
