# synthetic image feature detection using deep learning
## Aim:
to implement CNN based feature detector to detect corners in synthetic images genrated using opencv or some other method.
the some sample images used are shown below.
## sample input images used for training and testing
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Nonagon_ff03dd06-2a8a-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Pentagon_77780072-2a96-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Square_ff46205c-2a90-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Star_06b3c32c-2a86-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Triangle_827f38fa-2a87-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Star_06b5cc22-2a94-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Pentagon_78563260-2a92-11ea-8123-8363a7ec19e6.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/Triangle_829af6f0-2a8a-11ea-8123-8363a7ec19e6.png)

## Generating label using opencv:
1. Import datset to train 
2. **Generating label Images**: 
     * label image were generated using opencv "**Harris corner detector**". 
     * the corner point detected by harris corner detector were replaced by gaussian kernel.
      ![](https://i.imgur.com/zTwZ591.png)
     * thus the generated image is been used for training the network.
     * **image and label pair generated using above method:**
      <img src="https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/input%20and%20expected%20ouput.png" width="300" height="600" />

## network architecture:
Network Consist of encoder and decoder both constructed using structure similar to resnet's residual block which takes images as input and generate corner feature map as output shown below.
## results:
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_octagon.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_pentagon.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_square.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_triangle.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_star.png)
![](https://github.com/sushlokshah/synthetic-image-feature-detection-using-deep-learning/blob/main/pred_octagon.png)

## hyperparameters:

| Parameters | values |
| ---------- | ------ |
|    learning_rate        |     0.001   |
|     momentum       |   0.9     |
|        epoch    |    4    |
| batchsize  | 128    |

## Conclusion:
the network was successful in detecting feature-points given a raw image.
