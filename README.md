# MusicGenerator

## 개요

이 코드는 Siraj Raval 의 Deep Learning Nanodegree course with Udacity 라는 유투브 [영상](https://www.youtube.com/watch?v=pg9apmwf7og)을 기반으로 한 것입니다. 인코더와 디코더 모델을 이용해 입력된 MIDI 래그타임 곡을 바탕으로 MIDI 시퀀스를 생성할 것입니다.

## 종속성

프로그램은 아래를 필요로 합니다 (pip 로 설치하면 간단합니다):
 * 파이썬 3
 * 텐서플로우 (v0.10.0rc0 여야 하고, 이전 버전에서는 작동하지 않습니다)
 * CUDA (gpu 를 사용하기 위해서입니다, 텐서플로우 [설치 페이지](https://www.tensorflow.org/versions/master/get_started/os_setup.html#optional-install-cuda-gpus-on-linux) 를 참고하세요)
 * Numpy (텐서플로우와 함께 설치되어야 합니다)
 * Mido (midi 라이브러리)
 * Tqdm (깔끔한 진행 바를 위해 필요합니다)
 * OpenCv (파이썬 3 로는 간단한 설치 방법이 없고, 피아노 롤을 출력하기 위한 시각화 도구라 일종의 옵션입니다. 모든 OpenCv 호출은 imgconnector 파일에 포함되어 있어서 만약 OpenCv 를 사용하지 않으려면 파일 안의 함수를 제거하면 됩니다)

## 사용법

모델을 훈련하기 위해서는 간단히 `main.py` 를 실행하면 됩니다. 훈련한 이후에는 `main.py --test --sample_length 500` 로 결과를 생성할 수 있습니다. 더 많은 도움말과 옵션을 보려면 `python main.py -h` 를 실행하면 됩니다.

텐서보드를 이용해 그래프와 코스트를 보려면 `tensorboard --logdir save/` 를 실행하면 됩니다.


## 참조

이 코드는 [Conchylicultor](https://github.com/Conchylicultor/MusicGenerator)의 코드를 참조하여 알기 쉽게 편성한 것입니다.
