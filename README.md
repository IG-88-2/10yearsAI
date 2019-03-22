# 10yearsAI
This repository is containing 200.000 raw images and 100.000 preprocessed  10 years challenge images and implementation details.

## The Image Data ##
1 - You can use these datasets with providing the dataset publisher who is me :).
* [ The raw images (640x640) ](https://drive.google.com/open?id=1bp-UV0B3a5lmSqq0qjhmzFkktvelQATT "Raw Images")

2 - Preprocessed data ( This dataset has problem that some old and young images are in wrong class. The users should change it. It needs crowd sourcing. )
* [ Old Images (256x256) ](https://drive.google.com/open?id=1M_gaKmc97p7K0ychFK-5VP9qKp1fvoix "Old Images")
* [ Young Images(256x256) ](https://drive.google.com/open?id=1_IMPZxsuuAeet9MaB9uzgeUCXeLG9VMu "Young Images")

## Preprocess Details ## 
1 - Opencv face detector used to detect faces in the raw images. --> [ Face Detector](https://github.com/opencv/opencv/tree/master/samples/dnn/face_detector "Face Detector")

2 - The images have two faces detected and the faces are cropped.

3 - Face alignment is applied that uses affine transformation and Dlib face landmark detection. --> [ Face Alignment ](https://www.pyimagesearch.com/2017/05/22/face-alignment-with-opencv-and-python/ "Face Alignment") 

## Training Process ## 

1 - 994 preprocessed images is selected.

2 - pix2pix model is used for creating 10 years changed image.

3 - After 200 epochs and approximately 10 hours( I know the training dataset small and training is limited due to that I used Google Colab as a resource for training. ) 

## Some Results ##
* +13 :P
![Example](https://raw.githubusercontent.com/saitakturk/10yearsAI/master/1.JPG)

## Further Improvements and Limitations ##

* Due to high variability of faces that age and ethnicity difference, the head pose and glasses and other materials, I believe using head pose estimation will improve training results.

* Since the dataset is collected from internet, therefore, the images that is almost 10 years old. The image quality is relatively low quality to process.

* I will use more training images when I found time and computing power. Therefore, this repo will be updated...

