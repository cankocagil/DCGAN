# Deep Convolutional Generative Adversarial Network (DCGAN)

This repo implements the paper Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks (https://arxiv.org/abs/1511.06434) with slightly different and is based on the PyTorch Official DCGAN tutorial
(https://github.com/pytorch/examples/tree/master/dcgan) and used for practising purposes.

The dataset used for this repo is Large-scale CelebFaces Attributes (CelebA) Dataset. It has with more than 200K celebrity images, each with 40 attribute annotations. The images in this dataset cover large pose variations and background clutter. CelebA has large diversities, large quantities, and rich annotations, including

 * 10,177 number of identities,

 * 202,599 number of face images, and

 * 5 landmark locations, 40 binary attributes annotations per image.
 
 Dataset link :  http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
 
 
 This network consist of generator and discriminator networks. In generator model, we construct RGB images from gaussian noise by using following architecture
 

 ![DCGAN](https://user-images.githubusercontent.com/53329652/105554380-48fbec80-5d18-11eb-80d1-6551d7e943ea.png)
 
 
