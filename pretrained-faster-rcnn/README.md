The objective of this project is to do object detection using Faster Regional Convolutional Neural Network. Faster RCNN with backbone of ResNet-50 is used for detecting pedestrians. The model worked quite well with slight errors. It identifies a few random objects as pedestrians also. But overall, the model was extremely generalized, and it was able to detect all the pedestrians.

Following steps are used to produce below results:
1.)
Loading model=fasterrcnn_resnet50_fpn(pretrained=True) in evaluation mode.
2.)
Load the test video=PETS09-S2L1-raw.webm .
3.)
Capture the image frames= [1, 100, 200, 400] and convert them to tensors.
4.)
Fit model on the above converted image tensors and fetch the detections.
5.)
Filter out detections only for pedestrians with label=1.
6.)
Run non-maximal suppression with intersection of union value = 0.2 and 0.01 for two set of experiments.
