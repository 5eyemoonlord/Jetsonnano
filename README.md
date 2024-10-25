# Jetsonnano

https://sd-memory-card-formatter.en.softonic.com/download
balena Etcher로 이미지를 굽기 위한 준비 --balena Etcher프로그램 다운로드
-꽤 오래걸림,용량이 상당히 크므로 64GB이상의 SD카드를 이용했다
**jetpack**
**sd card formatter**
**balena etcher**도 다운로드 받았다

젯슨 나노에 SD카드를 넣고 와이파이 동글.키보드와 마우스 장착 후 **우분투**를 설치 했다
그 이후 영어로 설정,와이파이에 연결 후 지역은 서울로 설정 이렇게 하고 리붓을 하면 화면이 나온다.

이제 터미널을 켜서 쿨링 팬을 작동 시켰다.
쿨랑 팬을 작동시키기 위해서는 
sudo sh -c 'echo s128 > /sys/devices/pwm-fan/target_pwm'
을  입력한다.

카메라 연결 후 
nvgstcapture-1.0 --mode=2 —camsrc=0 --cap-dev-node=0
를 치면 카메라 화면이 젯슨 화면에 떴다


젯슨에 아키콘다를 설치했다.
설치할때
#!/bin/bash

wget https://github.com/build-tools/releases/download/0.2.3/Archicoda3-0.2.3/Archiconda-0.2.3-Linux-aarch64.sh
chmod +x Archiconda3-0.2.3-Linux-aarch64.sh
위 명령어를 사용하여 설치했다
결과가 잘나와서 다음 명령어를 입력했다.
conda env list
conda activate base
jetson_release 

이후 python3.8. 가상환경을 만들고 욜로 가상환경을 만들어 들어왔다
conda create -n yolo python=3.8 -y
conda env list
conda activate yolo

욜로 가상환경에 들어오니 (yolo)dli@dliL~$ 과같이 나타났다

 pip install -U pip wheel gdown

 gdown https://drive.google.com/uc?id=1hs9HM0XJ2LPFghcn7ZMOs5qu5HexPXwM

 gdown https://drive.google.com/uc?id=1m0d8ruUY8RvCP9eVjZw4Nc8LAwM8yuGV

 sudo apt-get install libopenblas-base libopenmpi-dev
sudo apt-get install libomp-dev
pip install torch-1.11.0a0+gitbc2c6ed-cp38-cp38-linux_aarch64.whl
pip install torchvision-0.12.0a0+9b5a3fe-cp38-cp38-linux_aarch64.whl
python -c "import torch; print(torch.__version__)"
하지만 오류가 발생하여 numpy를 다시 수동으로 설치해 주었다
conda install numpy

(yolo) dli@dli:~$ python

>>> import torch
>>> import torchvision
>>> print(torch.__version__)
>>> print(torchvision.__version__)
>>> print("cuda used", torch.cuda.is_available())
cuda used True
>>>
git clone https://github.com/Tory-Hwang/Jetson-Nano2
cd Jetson-Nano2/
cd V8
pip install ultralytics
pip install -r requirements.txt
pip install ffmpeg-python
sudo apt install tree
tree -L 2
을 쳤더니오류가 나서 리붓을 했다













