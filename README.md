# Visualizing 3D ResNet for Medical Image Classification With Score-CAM

 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/3d-viz-score-cam/blob/master/Visualizing_3D_ResNet_Medical_Image_Classification_With_Score_CAM.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


<div align="center">
    <a href="https://reshalfahsi.github.io/3d-viz-score-cam">
       <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/plot_00404.png" alt="architecture" >
       </img>
    </a>
    Live interaction with the 3D Score-CAM result.
    <br />
</div>

Intepretability is one of the concerns regarding the application of AI, or, to be exact, deep learning, in the medical field, especially medical image recognition. In a venture seeking to explain what is going on or what the network perceives computationally, one can leverage the class activation map (CAM) of the model. Score-CAM, one of the CAM variants, breakthroughs the preceding CAM methods by dropping the reliance on gradients. Instead, it benefits the full potential of the forward propagation of the model, running inference by normalized-weighting via element-wise product with the input. Then, the output logit of the target category is combined with the CAM acquired before to get the final outcome. In this project, the 3D version of ResNet is employed. To evaluate the aforementioned methods, the OrganMNIST3D dataset of MedMNIST is used. The deletion under the curve (DAUC) and the insertion under the curve (IAUC) are adopted to measure the performance of Score-CAM.


## Experiment

Catch up on this [link](https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/Visualizing_3D_ResNet_Medical_Image_Classification_With_Score_CAM.ipynb) to comprehend the training, testing, and visualization pertaining to this project.


## Result

### Image Classification

#### Quantitative Result

The table below exhibits the outcome, quantitatively.

Test Metric  | Score
------------ | -------------
Loss         | 0.570
Accuracy     | 89.79%


#### Accuracy and Loss Curve

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/acc_curve.png" alt="acc_curve" > <br /> Accuracy curves of 3D ResNet on the train and validation sets. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> Loss curves of 3D ResNet on the train and validation sets. </p>


### Visualization

#### Quantitative Result

Overall DAUC and IAUC scores of the Score-CAM on the 4th layer of 3D ResNet:

Test Metric  | Score
------------ | ----------------
DAUC         | 0.2576 ± 0.1710
IAUC         | 0.6750 ± 0.1944


#### Qualitative Result

The following are snapshots of the individual DAUC and IAUC scores and their Score-CAM outcomes.

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-bladder.png" alt="bladder" > <br /> The result of the bladder. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-heart.png" alt="heart" > <br /> The result of the heart. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-kidney-left.png" alt="kidney-left" > <br /> The result of the left kidney. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-kidney-right.png" alt="kidney-left" > <br /> The result of the right kidney. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-lung-left.png" alt="lung-left" > <br /> The result of the left lung. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-lung-right.png" alt="kidney-left" > <br /> The result of the right lung. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/3d-viz-score-cam/blob/master/assets/viz-spleen.png" alt="spleen" > <br /> The result of the spleen. </p>


## Citation

To cite this repository:

```
@misc{3dviz-scorecam,
   title = {Visualizing 3D ResNet for Medical Image Classification With Score-CAM},
   url = {https://github.com/reshalfahsi/3d-viz-score-cam},
   author = {Resha Dwika Hefni Al-Fahsi},
}
```


## Credit

- [Learning Spatio-Temporal Features with 3D Residual Networks for Action Recognition](https://arxiv.org/pdf/1708.07632)
- [Score-CAM: Score-Weighted Visual Explanations for Convolutional Neural Networks](https://openaccess.thecvf.com/content_CVPRW_2020/papers/w1/Wang_Score-CAM_Score-Weighted_Visual_Explanations_for_Convolutional_Neural_Networks_CVPRW_2020_paper.pdf)
- [RISE: Randomized Input Sampling for Explanation of Black-box Models](https://arxiv.org/pdf/1806.07421)
- [Interpretable Explanations of Black Boxes by Meaningful Perturbation](https://arxiv.org/pdf/1704.03296)
- [Score-CAM official code](https://github.com/haofanwang/Score-CAM)
- [MedMNIST v2-A large-scale lightweight benchmark for 2D and 3D biomedical image classification](https://arxiv.org/pdf/2110.14795)
- [MedMNIST official web page](https://medmnist.com/)
- [MedMNIST official code](https://github.com/MedMNIST/MedMNIST)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
