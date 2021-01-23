# Deep Convolutional Generative Adversarial Network (DCGAN)

This repo implements the paper Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks (https://arxiv.org/abs/1511.06434) with slightly different, is based on the PyTorch Official DCGAN tutorial (https://github.com/pytorch/examples/tree/master/dcgan. The ultimate aim of this repo is built alternative method for image augmentation for more complex visual object processing tasks such as,

* Facial Recognition
* Facial Landmark Localization
* Facial Expression Analysis and much more

via learning face images distributions so that new computer vision models can use DCGAN as a face generator.

A DCGAN is a direct extension of the GAN, except that it explicitly uses convolutional and convolutional-transpose layers in the discriminator and generator, respectively.[1] It was first described by Radford et. al. in the paper Unsupervised Representation Learning With Deep Convolutional Generative Adversarial Networks. The discriminator is made up of strided convolution layers, batch norm layers, and LeakyReLU activations. [1] The input is a 3x64x64 input image and the output is a scalar probability that the input is from the real data distribution. [1] The generator is comprised of convolutional-transpose layers, batch norm layers, and ReLU activations. [1]

The dataset used for this repo is Large-scale CelebFaces Attributes (CelebA) Dataset. It has with more than 200K celebrity images, each with 40 attribute annotations. The images in this dataset cover large pose variations and background clutter. CelebA has large diversities, large quantities, and rich annotations, including

 * 10,177 number of identities,
 * 202,599 number of face images, and

 
 Dataset link :  http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
 
 Here are some generated faces by DCGAN with 3 epochs:
 
 ![indir](https://user-images.githubusercontent.com/53329652/105556713-9ded3200-5d1b-11eb-9327-b0266c0a808c.png)
 
   
 This network consist of generator and discriminator networks. In generator model, we construct RGB images from gaussian noise by using the CNN following architecture 

 ![DCGAN](https://user-images.githubusercontent.com/53329652/105554380-48fbec80-5d18-11eb-80d1-6551d7e943ea.png)
 
 
 Then, discriminate the fake and real images by convolutional binary classifier with the following architecture (RHS):
 
![Whole-net](https://user-images.githubusercontent.com/53329652/105555102-bc522e00-5d19-11eb-84fb-ffd75c0d3008.png)
 

 Hence, end-to-end pipeline can be seen as:
 
 ![gan-overview](https://user-images.githubusercontent.com/53329652/105555254-0c30f500-5d1a-11eb-9a13-d23cb7711627.png)


In models section, there is a pretrained DCGAN model that is trained with 3 epochs.



Reference Link:

[1] https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html
