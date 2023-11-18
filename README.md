# Weakly Supervised Lung Disease Localization with Self-Supervised Representations and Mask-Guided Convolutional Networks

The Chest X-ray data is available on Kaggle: https://www.kaggle.com/datasets/nih-chest-xrays/data.

- The file named 'WSOL_maskguided_training.ipynb' consists of the main code for implementing the weakly supervised object localization framework.
- 'WSOL_AlignmentNetwork_K.ipynb' aligns the input chest X-ray images using the modified perceptual loss function.
- 'WSOL_Generate_Disease_Masks_K.ipynb' generates the disease masks used to guide the network and 'WSOL_Localization_Inference.ipynb' computes the localization performance of the WSOL framework. The alignment network and disease mask notebooks must be executed first to utilise them in the WSOL framework.

- In addition, the experiments conducted using various self-supervised learning models such as SimSIAM, Barlow Twins and VICReg are available in 'SSL_SimSIAM.ipynb', 'SSL_Barlow.ipynb', 'SSL_VICReg.ipynb' files respectively.
- The code used to fine-tune the self-supervised representations in a weakly supervised setting using the ResNet-50 backbone architectures defined by the authors of the SSL methods, is available in the file 'SSL_Finetune_ResNet50.ipynb'.

The code of the backbone ResNet-50 network used to perform the horizontal comparison of self-supervised learning methods such as SimSIAM, Barlow and VICReg was taken from their respective Github repositories mentioned in the papers. This was done to leverage the pre-trained self-supervised weights learned on ImageNet data by the methods trained for hundreds of epochs. Thus, the network layers have to match with the backbone in the WSOL framework in order to load the pre-trained ImageNet weights. In addition, the code used to initialise the self-supervised model and data augmentations was taken from https://github.com/lightly-ai/lightly.
