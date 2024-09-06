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
를 치면 카메라 화면이 젯슨 화면에 뜬다
