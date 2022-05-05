# ITI107 - Deep Neural Networks

## **Description**
- Object detection using transfer learning pretrained model (ssd resnet101 640x640)
- Small daaset of 100 images. Manual annotation using LabelImg tool using PascalVOC format.
- Training was done following step-by-step instructions from https://github.com/nyp-sit/iti107/blob/main/session-4/custom_training_with_tfod_api.md
    - Images and annotation files are copied to separate folders
    - Label map (.pbtxt file) of each numeric label to its corresponding text label was created
    - Images and annotations data was converted to TF Records binary format, with a train to validation split of 80% to 20%
    - Hyperparameter tuning (anchor aspect ratio, ratio of classification weight to localization weight) - object detection pipeline file was configured differently for separate runs of the training. 
    - Limited GPU memory allocated by instructor for training purposes, small batch of 4 used as a result
    - Highest mAP@IoU=0.50 of 0.643
- Object detection on out-of-sample test image and test video


## **Report excerpts**
[![Capture.png](https://i.postimg.cc/8C7YtjLg/Capture.png)](https://postimg.cc/VSc4Ns7K)

[![Capture.png](https://i.postimg.cc/Yq8y713w/Capture.png)](https://postimg.cc/pphBY540)

[![Capture.png](https://i.postimg.cc/wxQw5hns/Capture.png)](https://postimg.cc/bdd0p2yz)

[![Capture.png](https://i.postimg.cc/y8MhCdwH/Capture.png)](https://postimg.cc/zykHnJzt)

[![Capture.png](https://i.postimg.cc/L6qZ4Sk6/Capture.png)](https://postimg.cc/JGLhK9d9)
