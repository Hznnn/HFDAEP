# HFDAEP
The Code is created based on the method described in the following paper:
Zhuonan He, Jinjie Zhou, Dong Liang, Yuhao Wang, Qiegen Liu. Learning Priors in High-frequency Domain for Inverse Imaging Reconstruction

## Motivation
Ill-posed inverse problems in imaging remain an active research topic in several decades, with new approaches constantly emerging. Recognizing that the popular dictionary learning and convolutional sparse coding approaches are both essentially modeling the high-frequency component of an image, which convey most of the semantic information such as texture details, in this work we propose a novel multi-profile high-frequency transform-guided denoising autoencoder as prior (HF-DAEP). To achieve this goal, we first extract the multi-profile high-frequency components via a specific transformation and add the artificial Gaussian noise to these high-frequency components as training samples. Then, as the high-frequency prior information is learned, we incorporate it into classical iterative reconstruction process by proximal gradient descent technique. Preliminary results on highly under-sampled magnetic resonance imaging and sparse-view computed tomography reconstruction demonstrate that the proposed method can efficiently reconstruct feature details and present advantages over state-of-the-arts.

### Figs
![repeat-HFDAEPRec](https://github.com/yqx7150/HFDAEP/blob/master/figs/forward%20and%20backward.png)
Fig. 1. Demonstration of (a) the forward transform operator and (b) the backward transform operator in HF-DAEP.

![repeat-HFDAEPRec](https://github.com/yqx7150/HFDAEP/blob/master/figs/itermri.png)
Fig. 2. Illustration of HF-DAEP at iterative reconstruction phase. Here MRI reconstruction is visualized.

### Table

![repeat-HFDAEPRec](https://github.com/yqx7150/HFDAEP/blob/master/figs/table.png)

### Visual Comparisons
![repeat-HFDAEPRec](https://github.com/yqx7150/HFDAEP/blob/master/figs/result.png)
Fig. 3. Visual comparisons under 2D Random sampling at 80%. Top line: reference image, reconstruction using DLMRI, PANO and FDLCP; Bottom line: reconstruction using NLR-CS, DC-CNN, EDAEP and HFDAEP.

## Requirements and Dependencies
    caffe
    cuda 8.0
    
## MRI reconstruction
'./DemoMRI/demo_MRI.m' is the demo of HF-DAEP for MRI reconstruction.
## CT reconstruction
'./DemoCT/demo_CTRec.m' is the demo of HF-DAEP for CT reconstruction.
'./DemoCT/ultilies/generateSystemMatrix.m' is used to generate the system matrix.

## [<font size=5>**[Paper]**</font>](https://arxiv.org/ftp/arxiv/papers/1910/1910.11148.pdf)
    @article{he2019learning, 
    title={Learning Priors in High-frequency Domain for Inverse Imaging Reconstruction},
    author={He, Zhuonan and Zhou, Jinjie and Liang, Dong and Wang, Yuhao and Liu, Qiegen},
    journal={arXiv preprint arXiv:1910.11148},
    year={2019}
    }

## Other Related Projects
  * Multi-Channel and Multi-Model-Based Autoencoding Prior for Grayscale Image Restoration  
[<font size=5>**[Paper]**</font>](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8782831)  [<font size=5>**[Code]**</font>](https://github.com/yqx7150/MEDAEP)   [<font size=5>**[Slide]**</font>](https://github.com/yqx7150/EDAEPRec/tree/master/Slide)

  * Highly Undersampled Magnetic Resonance Imaging Reconstruction using Autoencoding Priors  
[<font size=5>**[Paper]**</font>](https://cardiacmr.hms.harvard.edu/files/cardiacmr/files/liu2019.pdf)  [<font size=5>**[Code]**</font>](https://github.com/yqx7150/EDAEPRec)   [<font size=5>**[Slide]**</font>](https://github.com/yqx7150/EDAEPRec/tree/master/Slide)

  * Denoising Auto-encoding Priors in Undecimated Wavelet Domain for MR Image Reconstruction  
[<font size=5>**[Paper]**</font>](https://arxiv.org/ftp/arxiv/papers/1909/1909.01108.pdf)  [<font size=5>**[Code]**</font>](https://github.com/yqx7150/WDAEPRec)

  * Complex-valued MRI data from SIAT--test31 [<font size=5>**[Data]**</font>](https://github.com/yqx7150/EDAEPRec/tree/master/test_data_31)

  * Complex-valued MRI data from SIAT--SIAT_MRIdata200 [<font size=5>**[Data]**</font>](https://github.com/yqx7150/SIAT_MRIdata200)
 
  * Learning Multi-Denoising Autoencoding Priors for Image Super-Resolution  
[<font size=5>**[Paper]**</font>](https://www.sciencedirect.com/science/article/pii/S1047320318302700)   [<font size=5>**[Code]**</font>](https://github.com/yqx7150/MDAEP-SR)

  * REDAEP: Robust and Enhanced Denoising Autoencoding Prior for Sparse-View CT Reconstruction  
[<font size=5>**[Paper]**</font>](https://ieeexplore.ieee.org/document/9076295)   [<font size=5>**[Code]**</font>](https://github.com/yqx7150/REDAEP)