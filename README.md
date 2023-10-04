# Object Detection using SSD Mobilenet and Tensorflow Object Detection API
This repository contains code for implementing object detection using the Single Shot MultiBox Detector (SSD) algorithm with TensorFlow. SSD is a popular real-time object detection algorithm known for its speed and accuracy. This implementation is built upon TensorFlow and provides a streamlined way to perform object detection on your own datasets or pre-trained models.

## SSD MobileNet Architecture
The SSD architecture is a single convolution network that learns to predict bounding box locations and classify these locations in one pass. Hence, SSD can be trained end-to-end. The SSD network consists of base architecture (MobileNet in this case) followed by several convolution layers

![Architecture](./media/arch.png)

By using SSD, we only need to take one single shot to detect multiple objects within the image, while regional proposal network (RPN) based approaches such as R-CNN series that need two shots, one for generating region proposals, one for detecting the object of each proposal. Thus, SSD is much faster compared with two-shot RPN-based approaches.

For more details about SSD architecture and its working, please read it’s official paper [here](https://arxiv.org/pdf/1512.02325.pdf)



## Results
Here are two examples of successful detection outputs on both images and videos:

![Image][1]

![Video][2]



| Model  | Training data                    | mAP Train | mAP VOC12 test |  Speed  |
|:------:|:--------------------------------:|:---------:|:--------------:|:-------:|
| vgg300 | VOC07+12 trainval and VOC07 Test |     79.5% |    [72.3%][3]  |   104   |
| vgg512 | VOC07+12 trainval and VOC07 Test |     82.3% |    [75.0%][5]  |   39    |

