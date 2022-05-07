# Comparing-GANs-for-Super-Resolution-of-LFW-Dataset

This repository looks at two open-source GAN models, [ESRGAN](https://github.com/xinntao/ESRGAN) and [GFPGAN](https://github.com/TencentARC/GFPGAN), and compares super resolution results on Labeled Faces in the Wild (LFW) Dataset. Specifically, I wanted to see the effect of super resolution using these models on face recognition accuracy results. 
To determine face recognition accuracy of the results, I used the Facenet face recognition model via the [Deepface repository](https://github.com/serengil/deepface). 
The notebook included shows one test that was performed. I used the "train" subset of labeled face pairs, which has 2200 pairs of faces (4400 images total). All 4400 images were super-resolved using ESRGAN, GFPGAN, and bicubic interpolation.
The unaltered images, as well as the super-resolved images using the three methods above, were passed into the Facenet model which predicts whether or not the pairs of faces are the same person or not. 
