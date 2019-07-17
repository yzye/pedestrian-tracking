# Pedestrian-Detection

This projects implement Object Detection based on Deep Learning by using the TensorFlow Object Detection API. It shows good performance of Object Detection models for inference, on Pedestrian Detection. 

<p align="center">
  <img src="/standing_output.gif" alt="Pedestrian Detector in action"></img>
</p>

### 1. Installation for TensorFlow Object Detection API
Refer to the instructions from this [link](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/install.html). This tutorial includes TensorFlow installation, environment setup, TensorFlow models installation and protobuf installation/compilation. To annotate training datasets, we should also need LabelImg installation. I would suggest to ceate virtual environment under Anaconda though it is not a requirement.

### 2. Data Preparation

We upload the test vedio `standing1.MP4` in `test_vedio` folder. And the output of the procesed vedio will locate at the same directory. We will extract frames from the vedio and put them into `test_images` directory. Then we implement the detection on every frame and the processed images would be saved. Finally we convert all processed images to a vedio.  

### 3. Model Selection

Tensorflow detection provides a collection of detection models pre-trained on the COCO dataset, the Kitti dataset, the Open Images dataset, the AVA v2.1 dataset and the iNaturalist Species Detection Dataset. We use these pre-trained models to make prediction on our test datasets. we can download the pre-trained models from [http://download.tensorflow.org/models/object_detection/](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md).I choose `faster_rcnn_resnet50_coco_2018_01_28` as default model which has the best performance on our datasets that I have ever tried. 

