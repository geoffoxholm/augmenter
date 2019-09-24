# Motivation
Data augmentation is used in machine learning to expand the number of examples in a dataset. 
For images, it is common to use image processing techniques like flipping, rotation, additive noise, alpha blending, and many others to slightly modify an image and add the edited image to the dataset. 


# Problem description

Your task is to **design a basic library to perform data augmentations for _paired_ image-to-image translation.** 
Datasets for paired image-to-image translation consists of images from a source domain A and images from some target domain(s) B<sub>i</sub> (i ≥ 1). 
This means that the dataset consists of a set of `N` input images from domain A and some number of other sets B<sub>i</sub> that contain `N` corresponding images in other modalities. 
For example, let's say you are training an image-to-image GAN which takes images of line drawings as input and generates images of watercolor paintings _and_ oil paintings.

## Requirements

Your solution should:
- be written in Python
- use a common image processing library like OpenCV (Python), Pillow, scikit-image
- use object-oriented techniques
- use appropriate and efficient data structures
- be designed as a stand-alone command-line application
- support running on 1 or more sets of images (where all sets have the same filenames but are contained in different directories)
- use a random number generator for each of the manipulations
- support at least 2 different image manipulations

## Example

For example, your application could be run like this:

```sh
   python3 augment.py data/sketches data/oil_paintings data/watercolor_paintings --output augmentations_output --count 10 
```

Which would create 10 different augmentations of each of the three directories of images. In each of these 10 augmentations some (random) amount of rotation and scaling (for example) will be applied. 


# Guidance

Feel free to extend the functionality of your program in any way that you want.
We realize that there's a lot of ambiguity in this assignment. 
Feel free to document what improvements you'd _like_ to make, but didn't budget time for.
Whatever code you do send, please make the effort to impress us with its quality. 
We'd rather see a small, but well-crafted example than an application with many features that was sloppily put together.
