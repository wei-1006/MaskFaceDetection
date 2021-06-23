# Mask-or-Non-Mask-Robust-Face-Mask-Detector-via-Triplet-Consistency-Representation-Learning
## This is the code of the paper Mask or Non-Mask? Robust Face Mask Detector via Triplet-Consistency Representation Learning presented in ACM TOMM

## Introduction
In the absence of vaccines or medicines to stop COVID-19, one of the effective methods to slow the spread of the coronavirus andreduce the overloading of healthcare is to wear a face mask. Therefore, we propose a face mask detection framework that uses the context attention module to enable the effective attention of the feedforward convolution neural network by adapting their attention maps feature refinement. Moreover, we further propose an anchor-free detector with Triplet-Consistency Representation Learning by integrating the consistency loss and the triplet loss to deal with the small-scale training data and the similarity between masks and occlusions.


## Overall Architecture
The proposed model consists of three losses, Center Loss, Triplet Loss, and Consistency Loss.
<img src="images/losses.png" width="750">

CBAM modules are included to imporve the performance of the model.
<img src="images/resnet_cbam.png" width="750">

## Dataset

## Training

## Performance
Perforamcen on the AIZOO dataset

<table>
  <tr>
    <td>Model</td>
    <td colspan="2">Face</td>
    <td colspan="2">Mask</td>
  </tr>
  <tr>
    <td></td>
    <td>Precision</td>
    <td>Recall</td>
    <td>Precision</td>
    <td>Recall</td>
  </tr>
  <tr>
    <td>AIZOOTech</td>
    <td>89.6</td>
    <td>85.3</td>
    <td>91.9</td>
    <td>88.6</td>
  </tr>
  <tr>
    <td>RetinaMask + MobileNet</td>
    <td>83.0</td>
    <td>95.6</td>
    <td>82.3</td>
    <td>89.1</td>
  </tr>
  <tr>
    <td>RetinaMask + ResNet50</td>
    <td>91.9</td>
    <td>96.3</td>
    <td>93.4</td>
    <td>94.5</td>
  </tr>
  <tr>
    <td>CenterFace + MobileNet(ours)</td>
    <td>96.8</td>
    <td>88.0</td>
    <td>88.0</td>
    <td>95.2</td>
  </tr>
  <tr>
    <td>CenterFace + ResNet18(ours)</td>
    <td>99.3</td>
    <td>96.2</td>
    <td>99.7</td>
    <td>96.7</td>
  </tr>
</table>

Performance on WIDER FACE and MAFA datasets

<table>
  <tr>
    <td>Model</td>
    <td colspan="3">WIDER FACE</td>
    <td>MAFA</td>
  </tr>
  <tr>
    <td></td>
    <td>Easy</td>
    <td>Medium</td>
    <td>Hard</td>
    <td></td>
  </tr>
  <tr>
    <td>RetinaMask + ResNet50</td>
    <td>59.4</td>
    <td>48.9</td>
    <td>26.5</td>
    <td>94.5</td>
  </tr>
  <tr>
    <td>CenterNet + ResNet18</td>
    <td>72.6</td>
    <td>71.4</td>
    <td>46.0</td>
    <td>91.5</td>
  </tr>
  <tr>
    <td>CenterNet + ResNet18 + CBAM</td>
    <td>19.4</td>
    <td>19.6</td>
    <td>10.4</td>
    <td>22.4</td>
  </tr>
  <tr>
    <td>CenterNet + ResNet18 + triplet loss</td>
    <td>76.4</td>
    <td>74.0</td>
    <td>47.1</td>
    <td>91.0</td>
  </tr>
  <tr>
    <td>CenterNet + ResNet18 + consistency loss</td>
    <td>74.0</td>
    <td>72.2</td>
    <td>45.6</td>
    <td>91.8</td>
  </tr>
  <tr>
    <td>CenterNet + ResNet18 + triplet loss + consistency loss</td>
    <td>75.8</td>
    <td>73.0</td>
    <td>46.3</td>
    <td>91.4</td>
  </tr>
  <tr>
    <td>CenterFace</td>
    <td>90.02</td>
    <td>85.4</td>
    <td>54.1</td>
    <td>91.5</td>
  </tr>
</table>

