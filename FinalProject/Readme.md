# Generating Adversarial inputs for LPR systems(DSCI-6672-AI-DS-Cyber-Security-Final Project)
#Generating adverserial inputs for License plate recognition systems

Final Project for  DSCI-6672-AI-DS-Cyber-Security- University of New Haven

Introduction:

This Project consists of the License plate Recognition Models and then perturbing a individual integer as an input for adversarial attacks.

The dataset is ReID and is explained detailly below.

The image processing techniques have been adapted from several scholars of github .



I have tried to perturb the whole license plate in as a single input but due to some technical limitations as of now for the strides . Unable to convert strides of 3 or 1 to 2.

So instead we go with the process of perturbing the sgregated images.
Segregated images are individual images that are segregated form license plates . They are cleaned filtered and then segregated. This model is adverserially attacked if we can paste the perturbed images shown in the ipynb onto a valid license plate. And we should test the plate with the same model not any other model. 

As we have created the perturbation based on the model this wpould be considered white box attack .


# File desc:

LPR.ipynb has the steps for building a model training  and saving the models  to h5 files. It also has the perturbation concepts and adverserially created images.

lpr_image_processing.py has below functions that are adapted for several github scholars.

def image_extraction(csv_files, channel):
    """
    the images to be extxracted are grayscale
    extract images from images/grayscale
    """

def homomorphic_filter(csv_files):
    """
    to improve the area of observation in the license plate.
    this function removes a lot of noise and unnecessary parts of the
    license plate


def MSER():
    """
    Maximally Stable External Region extractor
    character segmentation algorithm
    only draws contours around the alphabets
    """


def get_component(data, i, j):
    """
    returns a single component which is in the same component as i,j in the pixel
    #set data[i][j] = 0 so that it will not go to an infinite loop
    image will be sent as reference and BE AWARE,
    once you call this image will be BLACK every where.
    so if you want to store the original image some where
    make sure to copy in another variable
    """


def get_segments(data):
    """
    sends an array of segmented images, provided the data has only 0->black and 255->white.
    image will be sent as reference and BE AWARE,
    once you call this image will be BLACK every where.
    so if you want to store the original image some where
    make sure to copy in another variable
    """


def print_segments(segments):
    """
    use the segments and re-create the images using the segments
    """

def convert_image_to_numpy(individual):
    """
    convert image to array
    """

def save_filtered_data(copy_filtered_data, labels):
    """
    save the filtered homomorphic images in images/filtered
    """

def filtered_image_extraction(files):
    """
    extract images from images/filtered
    """

def noise_removal(copy_X, index):
    """
    remove the remaining noisy parts from homomorphed images
    """


def flip_and_rotate():
    """
    flip and rotate the images
    """


def final_extraction(folder_list):
    """
    extract images from all folder from training all characters
    AVAILABLE CHARACTERS - 0 1 2 3 4 5 6 7 8 9
                           A B C D E F I J L M N
                           P R S T V W X Z
    """

def image_padding_by_resize(data, pad_x, pad_y):
    """
    padding by resizing
    performs very poor because image resolution is poor
    can be used if the data is highly pixelated
    """

def preparing_data():
    """
    image extraction and processing
    1. Homomorphic filter is applied on all images & saved in images/filtered
    2. Segmenting the homomorphed images and extracting each
       character from the images
    3. Saving these segmented image to images/segmented
       The character has to be manually re-arranged into folders
       Each folder name is the character shown in the image
    """






# Next steps

The next steps would be to make this a black box attack if possible and do it for the complete license plate as input instead of the segregated images of each.

         




CITATION
========
@INPROCEEDINGS
{
Spanhel2017holistic, 

  author={{\v{S}}pa{\v{n}}hel, Jakub and Sochor, Jakub and Jur{\'a}nek, Roman and Herout, Adam and Mar{\v{s}}{\'\i}k, Luk{\'a}{\v{s}} and Zem{\v{c}}{\'\i}k, Pavel},
  
  booktitle={2017 14th IEEE International Conference on Advanced Video and Signal Based Surveillance (AVSS)},
  
  title={Holistic recognition of low quality license plates by CNN using track annotated data}, 
  
  year={2017}, 
  
  pages={1-6},
  
  keywords={Character recognition;Image recognition;Image segmentation;Licenses;Neural networks;Optical character recognition software;Training},
  
  organization={IEEE},
  
  doi={10.1109/AVSS.2017.8078501}, 
  
  ISBN={978-1-5386-2939-0}, 
  
  month={Aug},
  
  year={2017}
  
}



****************
* DATASET INFO *
****************


Ground truth labels, train/test split
============
File: trainVal.csv
------------

track_id - ID of specific track based on tracker

image_path - path to image in archive structure

lp - ground truth text for license plate

train - Train/test split. 0 - test, 1 - train

