# Preprocessing-of-Image-datasets

Data Collection Plan
Stage one datasets are validated, peer-reviewed, and made available for academic purposes. 
These datasets are processed to label eight familiar landmarks for both datasets. 
JAFFE datasets are grayscale, whereas some CK+ datasets are in color; therefore, all color images are converted to grayscale for consistency


Raw Dataset Samples
The JAFFE dataset consists of 213 images with seven labels: fear, sadness, happiness, surprise, anger, disgust, and neutral. 
Raw samples of the JAFFE dataset are shown in Figure 15. The CK+ dataset consists of 969 images with seven labels: fear, sadness, happiness, 
surprise, anger, disgust, and contempt. Raw samples of CK+ dataset are shown in Figure 16. Both datasets have six standard labels and 
one different label: neutral and contempt, so the total number of labels is eight. The format of JAFFE is TIFF, and all images
have the exact resolution, 256 by 256. The format of CK+ is PNG, and there are three resolutions 640 by 490, 640 by 480, and 720 by 480.

Data Transformation
The act of transforming, purifying, and organizing data into a proper format that can be studied to support decision-making procedures and to spur an organization's growth is known as data transformation. When data needs to be modified to conform to the requirements of the target system, it is used. At the enterprise level, various pricey and open-source Extract, Transform, Load (ETL) solutions are employed to provide the needed outputs. For example, image transformation is done during image processing to change an image from one dimension to another. Finding features that may be difficult to see in image space requires viewing an image in three dimensions. In this project, the team uses image smoothing, image normalization, and image regularization techniques. The team also uses affine and singular value decomposition techniques, image resizing, gray scaling, horizontal flipping, and rotation for image modification.
To make an image more recognizable, the team does image normalization, which entails altering the range of pixel intensity values. Image normalization is frequently used to eliminate noise from images. High-frequency and very low noise can be removed from an image with image normalization, which is very beneficial. The goal is to restore the image's contrast if it becomes low for any causes.
The team normalizes the images using Python's "cv2.normalize()" function from the cv2 library. First, the images are read using the imread() function. Following that, the team uses the NumPy function "np.zeros()" to create a new array of size 256*256. The cv2.normalize() function is then used to normalize the data in an array. The function's first parameter is the image's name, followed by the normalizing criteria. The second parameter is zero, and the third parameter is 255, which marks the lower and upper limit values in the array, respectively. Finally, the last parameter is cv.NORM_MINMAX; in this case, alpha and beta are the lower and higher values. The team chooses to use min-max normalization because it saves the relationship between the values in the array by selecting the lowest value as zero and the highest value as one. ![image](https://user-images.githubusercontent.com/58579913/210539481-c0e74d61-8724-4875-8905-476f046fd334.png)



