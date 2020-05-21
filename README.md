## ACSE 4.4 - Machine Learning Miniproject
## The Identification Game
#### Team Sigmoid: Hanchao Chen, Mia Chen, Helen Situ, Nicolas Trinephi, Ke Wen

![image](https://i.ibb.co/myQ1g49/AAAADATA.png)

This repository contains two Jupyter Notebooks for the final two submissions to [The Identification Game Kaggle competition](https://www.kaggle.com/c/acse-miniproject/overview) by Team Sigmoid, as part of the ACSE-4 2019/20 module.

### User Instructions & Requirements

The software dependencies can be found in the `requirements.txt` file in this repository. We recommend having at least 12GB of available GPU RAM available when running the notebooks.

The most straightforward way to run the notebooks is via Google Colab. Simply open [Google Colab](https://colab.research.google.com/), log into or create a Google account, select `File > Open notebook > GitHub` and paste the URL of this repository to load the notebooks. Then, select `Runtime > Change runtime type` and change the hardware accelerator to GPU. Once loaded, all cells can be run in order. The notebook will download the dataset used in this project. These notebooks are very memory-heavy in exchange for performance, but the standard allocated 12GB from Colab should be more than enough.

If run on a local machine, we recommend using Conda. Please set up PyTorch by running the following commands:
```
conda create -n torch-env
conda activate torch-env
conda install -c pytorch pytorch torchvision cudatoolkit=10
```
Then navigate to the directory containing the contents of this repository and run the following command to install the rest of the dependencies:
```
conda install --file requirements.txt
```
And run the following to open the notebooks.
```
jupyter notebook
```
Once opened, run all the cells. The notebook will download the dataset used in this project. 

### Documentation

Please refer to `Documentation.txt` for the full documentation of classes and functions defined in the code.

### Dataset

A dataset of 100000 JPEG images (mostly RGB) of dimension 64 x 64 belonging to 200 classes was provided as the training set for this project. A separate set of 10000 JPEG images of the same dimension was provided as the test set. Refer to https://www.kaggle.com/c/acse-miniproject/overview for more information. 

### Models

The two convolutional neural network architectures used in the final submissions were EfficientNet-B7 and ResNet152, both pre-trained on the ImageNet dataset. 

#### EfficientNet
EfficientNet ([Tan & Le, 2019](https://arxiv.org/abs/1905.11946/)) was created with the idea to balance network depth, width and resolution to achieve higher performance at much higher efficiency than other networks. In this project, the PyTorch implementation of EfficientNet pretrained on ImageNet found [here](https://github.com/lukemelas/EfficientNet-PyTorch/) was used to achieve a final macro F1-score of ___.


#### ResNet151
Residual Neural Networks (ResNet) ([He et al, 2016](https://arxiv.org/pdf/1512.03385.pdf)) build on the idea of skipping layers and adapting the skipped weights to speed up training. In this project, the `torchvision.models` implementation of a pre-trained ResNet152 was used to achieve a final macro F1-score of ___.


### Acknowledgements
We would like to thank the ACSE-8 and ACSE-4 teaching teams and GTAs for providing and overseeing an enjoyable project and delivering an invaluable learning experience remotely despite unfortunate circumstances due to COVID-19. Additionally, we would like to thank Google Colab for providing the computing resources that made this project possible, as well as the developers of PyTorch, Torchvision and EfficientNet PyTorch. 

### License

This software is published under the MIT License.

### References

He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 770-778).

Tan, M., & Le, Q. V. (2019). Efficientnet: Rethinking model scaling for convolutional neural networks. arXiv preprint arXiv:1905.11946.




