# Database-for--CBIR-system-Matlab-
Creating database using unstructured data to be used in a  Content-Based Image Retrieval system that helps find images based on their content, using annotations to describe what's in the pictures.

INTRODUCTION 
CBIR (Content-Based Image Retrieval) lets you find images based on their content, not just their descriptions. To make this work well, we need to do three key things: preprocess the images, add relevant information (annotation), and pick out important features that describe what's in the images. 

CBIR aims to make finding images easier by focusing on their visual content, not just words. It's handy for things like image search engines and medical image analysis. 


METHODOLOGY, FUNCTION USED FOR STORAGE 
Image Collection (Task 1): 
I started by specifying the folder path where images are stored and uses a wildcard pattern to gather file information about JPEG images in the directory. A loop is then initiated to process each image individually. Images are collected from a specified folder using the dir. function and stored in a structure array. 
Image Preprocessing (Task 2): 
In this part, for each image, a part of code for preprocessing steps are applied inside a loop. These include resizing the image to a uniform size of 500x500 pixels, converting it to grayscale, and denoising using Gaussian filtering. The pre-processed images are saved in a separate folder at each step.  
Feature Extraction (Task 4): 
In this part, I calculated statistical features (mean, standard deviation, skewness) for each color channel (red, green, blue) of the resized image. These features are stored in a table, and the information is encoded into a JSON file. Additionally, Gabor filtering is applied to the grayscale image, and the magnitude and phase of the Gabor response are visualized in a subplot layout for clear visualisation. 
Image Annotation (Task 3): 
In this part a metadata is created named Image metadata, including filenames, keywords, and 
descriptions,  which information are all manually assigned outside the loop for all 28 images. This 
information is stored in a cell array and later converted into a table. The table is saved as a MAT file 
for future use.
