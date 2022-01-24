# Mediapipe examples

From:
https://google.github.io/mediapipe/


## Installation

```
python -m venv env
source env/bin/activate
pip install -r requirements.txt
```

For the iris example, download `iris_landmark.tflite` into `models` directory:
```
wget -P models https://github.com/google/mediapipe/raw/master/mediapipe/modules/iris_landmark/iris_landmark.tflite
```

## How to run

One of the following:

```
python face_detection.py
python face_mesh.py
python hands.py
python head_posture.py
python holistic.py
python iris.py
python objectron.py
python pose.py
python selfie_segmentation.py
```

`pose.py` and `iris.py` include the possibility to process a video file instead of the webcam input stream. Run like this:

```
python iris.py -i /path/to/some/file/i-am-a-video-file.mp4
python pose.py -i /path/to/some/file/i-am-a-video-file.mp4
```

## Numpy

See example `python pose.py` for how to extract numpy array from the mediapipe landmark objects.

## Running Tests for New Iris Tracking Intake
1. set the name of the persisting file you want to use on line 175 of iris.py
```
       with open('csvs/testdeltas.csv', mode='a', newline='') as f:
```
2. run `python iris.py`


## Running Tests for New Iris Tracking
1. set the name of the model you want to use on line 72 of iris tester
```
       with open('iris_model_16_2_5_gb_kfolds.pkl', 'rb') as f:
```
2. run `python iris_tester.py`