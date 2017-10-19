## gsv2pv
A deep learning pipeline for estimating pedestrian volume with google street views. For getting GSV images, use [streetscape](https://github.com/yonghah/streetscape)

# Set up

### 1. Clone repository
```
git clone git@bitbucket.org:yongha_hwang/gsv2pv.git
cd gsv2pv
```

### 2. Install TensorFlow, Google Object Detection API and download model

##### Install TensorFlow

See https://www.tensorflow.org/install/

##### Install Google object detection API 
```
bin/init.sh
```

### 3. Install dependencies
```
sudo pip install pillow
sudo pip install lxml
sudo pip install jupyter
sudo pip install matplotlib
```

### 4. Protobuf compilation
```
cd models/research
protoc object_detection/protos/*.proto --python_out=.
```

### 5. Add libraries to python path
```
# from models/research
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```
Note: This command needs to run from every new terminal you start. If you wish to avoid running this manually, you can add it as a new line to the end of your ~/.bashrc file.


### 6. Install GSV
```python
# from repo root
pip install .
```
