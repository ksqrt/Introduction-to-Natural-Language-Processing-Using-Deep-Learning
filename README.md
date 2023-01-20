

# 1 . 진행환경설정

딥러닝을 시작할때 가장 큰 진입장벽은 환경설정입니다.

CUDA 와 CUDNN , TensorFlow 버전의 서로 간 호환성이 좋지 않기 때문에 초기 환경설정에 많은 시간과 노력이 들어갑니다.

따라서 환경설정에 들어가는 시간을 줄이고자
미리 CUDA, CUDNN , TensorFlow 의 환경설정이 완료된 이미지를 
도커허브에서 pull 해와서 사용 해보았습니다.

사용된 이미지 

https://hub.docker.com/r/datamachines/cudnn_tensorflow_opencv


명령어

```
docker pull datamachines/cudnn_tensorflow_opencv:11.6.2_2.9.1_4.6.0-20220815
```
