
## **1 . 환경설정**

딥러닝을 시작할때 가장 큰 진입장벽은 환경설정입니다.

CUDA 와 CUDNN , TensorFlow 버전의 서로 간 호환성이 좋지 않기 때문에 초기 환경설정에 많은 시간과 노력이 들어갑니다.

따라서 환경설정에 들어가는 시간을 줄이고자 미리 CUDA, CUDNN , TensorFlow 의 환경설정이 완료된 이미지를 도커허브에서 pull 해와서 사용 해보겠습니다.

### 사용된이미지

도커허브 : https://hub.docker.com/r/datamachines/cudnn_tensorflow_opencv

깃허브 : https://github.com/datamachines/cuda_tensorflow_opencv/tree/20220815

이미지의 pulls 는 100K 이상으로 많은 데이터관련 작업시 사용되고 있는듯 합니다

### 이미지의 버전 목록

| Docker Tag | CUDA | CUDNN | TensorFlow | OpenCV | Ubuntu | Github Link | OpenCV  | TensorFlow  | FFmpeg  | PyTorch  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 11.3.1_2.9.1_3.4.16-20220815 | 11.3.1 | 8.2.0 | 2.9.1 | 3.4.16 | 20.04 | https://github.com/datamachines/cuda_tensorflow_opencv/tree/20220815 | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815-OpenCV.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815-TensorFlow.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815-FFmpeg.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_3.4.16-20220815-PyTorch.txt |
| 11.3.1_2.9.1_4.6.0-20220815 | 11.3.1 | 8.2.0 | 2.9.1 | 4.6.0 | 20.04 | https://github.com/datamachines/cuda_tensorflow_opencv/tree/20220815 | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815-OpenCV.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815-TensorFlow.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815-FFmpeg.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.3.1_2.9.1_4.6.0-20220815-PyTorch.txt |
| 11.6.2_2.9.1_3.4.16-20220815 | 11.6.2 | 8.4.0 | 2.9.1 | 3.4.16 | 20.04 | https://github.com/datamachines/cuda_tensorflow_opencv/tree/20220815 | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815-OpenCV.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815-TensorFlow.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815-FFmpeg.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_3.4.16-20220815-PyTorch.txt |
| 11.6.2_2.9.1_4.6.0-20220815 | 11.6.2 | 8.4.0 | 2.9.1 | 4.6.0 | 20.04 | https://github.com/datamachines/cuda_tensorflow_opencv/tree/20220815 | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815-OpenCV.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815-TensorFlow.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815-FFmpeg.txt | https://github.com/datamachines/cuda_tensorflow_opencv/blob/master/BuildInfo/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815/cudnn_tensorflow_opencv-11.6.2_2.9.1_4.6.0-20220815-PyTorch.txt |

### 명령어

```bash
docker pull datamachines/cudnn_tensorflow_opencv:11.6.2_2.9.1_4.6.0-20220815
```

## **2 . 부족한 필수 라이브러리 설치**

### 1. 젠심
젠심(Gensim) 은 머신 러닝을 사용하여 토픽 모델링과 자연어 처리 등을 수행할 수 있게 해주는 오픈 소스 라이브러리입니다. 

```
#  젠심 설치
pip install gensim

```
### 2.  NLTK와 NLTK Data 설치
엔엘티케이(NLTK)는 자연어 처리를 위한 파이썬 패키지입니다. 보통
아나콘다에 설치되어있지만 이 환경에서는 없기 때문에 설치합니다

```
# NLTK와 NLTK Data 설치
pip install nltk
```

### 3. KoNLPy 설치
코엔엘파이(KoNLPy)는 한국어 자연어 처리를 위한 형태소 분석기 패키지입니다.
우리는 한국인이기떄문에 ... 꼭 설치합시다.
참고로 KoNLPy 의 경우 우분투 지원 버전이 다르지만 
아직까지 문제 발생하지 않음 

```
# KoNLPy를 위한 JAVA 설치
apt install default-jdk
```

```
# KoNLPy 설치
pip install konlpy
```

### 4. 판다스 프로파일링 설치

EDA(Exploratory Data Analysis, 탐색적 데이터 분석)를 위한 라이브러리 설치
```
pip install -U pandas-profiling
```

### 5.
