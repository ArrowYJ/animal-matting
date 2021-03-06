<!-- # animal-matting -->
# End-to-end Animal Image Matting
<!-- by
Author 1,
Author 2,
etc -->

<!-- ## Introduction -->

<p align="justify">This repository contains the code, datasets, models, test results and a video demo for the paper <a href="https://arxiv.org/pdf/2010.16188.pdf">End-to-end Animal Image Matting</a>. We propose a novel Glance and Focus Matting network (<strong>GFM</strong>), which employs a shared encoder and two separate decoders to learn both tasks in a collaborative manner for end-to-end animal matting. We also establish a novel Animal Matting dataset (<strong>AM-2k</strong>) to serve for end-to-end matting task. Furthermore, we investigate the domain gap issue between composition images and natural images systematically, propose a carefully designed composite route <strong>RSSN</strong> and a large-scale high-resolution background dataset (<strong>BG-20k</strong>) to serve as better candidates for composition.</p>

[Here](https://drive.google.com/file/d/1-NyeclNim9jAehrxGrbK_1PbFTgDZH5S/view?usp=sharing) is a video demo to illustrate the motivation, the network, the datasets, and the test results on an animal video.

The paper is currently under review. All the datasets (**AM-2k** and **BG-20k**), training code, test code, and the pretrained models will be made publicly soon.


## GFM
The architecture of our proposed end-to-end method <strong>GFM</strong> is illustrated below. We adopt three kinds of <em>Representation of Semantic and Transition Area</em> (<strong>RoSTa</strong>) `-TT, -FT, -BT` within our method. 
![](demo/src/gfm.png)

We trained GFM with three backbones, `-(d)` [DenseNet-121], `-(r)` [ResNet-34], and `-(r2b)` [ResNet-34 with 2 extra blocks]. The trained model for each backbone can be downloaded via the link listed below.


| GFM(d)-TT | GFM(r)-TT | GFM(r2b)-TT|
| :----:| :----: | :----: | 
|coming soon|coming soon|coming soon| 


## AM-2k
Our proposed <strong>AM-2k</strong> contains 2,000 high-resolution natural animal images from 20 categories along with manually labeled alpha mattes. Some examples are shown as below, more can be viewed in the [video demo](https://drive.google.com/file/d/1-NyeclNim9jAehrxGrbK_1PbFTgDZH5S/view?usp=sharing).
![](demo/src/am2k.png)

## BG-20k
Our proposed <strong>BG-20k</strong> contains 20,000 high-resolution background images excluded salient objects. Some examples are shown as below, more can be viewed in the [video demo](https://drive.google.com/file/d/1-NyeclNim9jAehrxGrbK_1PbFTgDZH5S/view?usp=sharing).
![](demo/src/bg20k.jpg)

## Results Demo

We test GFM on our AM-2k test dataset and show the results as below. More results on AM-2k test set can be found [here](https://github.com/JizhiziLi/animal-matting/tree/master/demo/).

<img src="demo/src/sample3.jpg" width="50%"><img src="demo/src/sample3.png" width="50%">

<img src="demo/src/sample1.jpg" width="50%"><img src="demo/src/sample1.png" width="50%">

<img src="demo/src/sample2.jpg" width="50%"><img src="demo/src/sample2.png" width="50%">


## Statement
This project is for research purpose only, please contact us for the licence of commercial use. For any other questions please contact [jili8515@uni.sydney.edu.au](mailto:jili8515@uni.sydney.edu.au).

