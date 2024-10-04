# Face Detection AI Project

face-detection-adas-0001
Use Case and High-Level Description
Face detector for driver monitoring and similar scenarios. The network features a default MobileNet backbone that includes depth-wise convolutions to reduce the amount of computation for the 3x3 convolution block.


Inputs
Image, name: data, shape: 1, 3, 384, 672 in the format B, C, H, W, where:

B - batch size

C - number of channels

H - image height

W - image width

Expected color order is BGR.

Outputs
The net outputs blob with shape: 1, 1, 200, 7 in the format 1, 1, N, 7, where N is the number of detected bounding boxes. The results are sorted by confidence in decreasing order. Each detection has the format [image_id, label, conf, x_min, y_min, x_max, y_max], where:

image_id - ID of the image in the batch

label - predicted class ID (1 - face)

conf - confidence for the predicted class

(x_min, y_min) - coordinates of the top left bounding box corner

(x_max, y_max) - coordinates of the bottom right bounding box corner
