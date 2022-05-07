# Comparing-GANs-for-Super-Resolution-of-LFW-Dataset

This repository looks at two open-source GAN models, [ESRGAN](https://github.com/xinntao/ESRGAN) and [GFPGAN](https://github.com/TencentARC/GFPGAN), and compares super resolution results on Labeled Faces in the Wild (LFW) Dataset. Specifically, I wanted to see the effect of super resolution using these models on face recognition accuracy results. 
To determine face recognition accuracy of the results, I used the Facenet face recognition model via the [Deepface repository](https://github.com/serengil/deepface). 
The notebook included shows one test that was performed. I used the "train" subset of labeled face pairs, which has 2200 pairs of faces (4400 images total). All 4400 images were super-resolved using ESRGAN, GFPGAN, and bicubic interpolation.
The unaltered images, as well as the super-resolved images using the three methods above, were passed into the Facenet model which predicts whether or not the pairs of faces are the same person or not. 
Initial results show that the recognition performance for the LFW dataset was the best for the unaltered low resolution (LR) images. ESRGAN was next in performance, then bicubic interpolation, then GFPGAN. 
These results are surprising based on the perceptual quality of the images shown below. 

## Some representative results using colored and cropped LFW images
![color2](https://user-images.githubusercontent.com/95577984/167269199-c9c40129-7ea9-4e2a-a50a-ca0ac166b41f.png)
![color3](https://user-images.githubusercontent.com/95577984/167269205-3e2b0f88-dd03-4a68-bfe3-8b5ba930d28c.png)
![color5](https://user-images.githubusercontent.com/95577984/167269209-2ed2b9da-bdd2-4bf2-b2f2-261de4b0a07c.png)
![color6](https://user-images.githubusercontent.com/95577984/167269212-c538eed1-4db8-4af4-9178-23f78acca2a1.png)
## Some representative results using Black and White and cropped LFW images
![BW1](https://user-images.githubusercontent.com/95577984/167269235-defde1d3-4850-4ec1-976b-3dbfb6ce09c7.png)
![BW2](https://user-images.githubusercontent.com/95577984/167269237-49639e04-43b9-4865-8aaa-4dd8240c5942.png)
![BW3](https://user-images.githubusercontent.com/95577984/167269238-0a49ab81-e400-43b5-8a96-2d516aa7eee8.png)
![BW4](https://user-images.githubusercontent.com/95577984/167269242-c8a2e64c-406a-45c3-a9a1-39cdf1403b1c.png)
