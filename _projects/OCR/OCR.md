---
layout: project
title: Optical Character Recognition for text-to-LaTex Conversion
permalink: /projects/OCR
subtitle:
rollover-text:
project-type: engineering
project-priority: 9
cover-img: OCR1.png
images:
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
 - image_path: /projects/OCR/OCR2.jpg
---
## Overview
The goal for this project was to implement python machine learning packages to develop an Optical Character Recognition algorithm that could take in images of handwritten math equations, accurately identify each symbol in the equation, and output a LaTex representation. Optical Character Recognition (OCR) is the industry term for the technology that allows people to capture and convert text in an image to machine-readable text. For those who are unfamiliar, LaTex is a popular text editor that academics use often to write mathematical equations inline with document text.

The motivation for this project stems from the requirements of one of my graduate math courses where it was course policy that homework solutions be type-written. Having been new to the LaTex text editor, this policy caused me great frustration because typing up complex algebraic expressions almost doubled the time I spent on one assignment!

There were two main functional objectives for this project: 1) character classification using a CNN and 2) text-to-LaTex conversion. The dataset used to train the ML model was a set of 82 alphanumeric character classes (i.e. 0-9, +, -, <, >, /, *, etc.) consisting of a total 375,974 unique handwritten character images distributed among those classes. Image1 in the carousel shows sample images from each character class and also depicts the results image pre-processing (purple background).

## Character Classification
A Convolution Neural Network architecture was developed as the machine learning model for this project. The architecture that was used closely emulated the well-known LeNet-5 CNN architecture (illustrated in Image2) which uses a series of convolution and sub-sampling layers. The raw dataset was split into test and train sets and the model was trained over a period of 100-epochs, taking around 8hrs to complete! 

The training prediction accuracy and loss plots are shown in the carousel. The resulting prediction accuracy of the model was computed to be around 0.9913. 

As an intermediate result, random sample images from each character class in the test set were passed through the model. The model demonstrated adequate ability to predict each symbol's character class with minimal inaccuracies -- for example, if the input image was the division sign: &#247;, then the prediction would be "div".

Using the model to predict individual character classes from singular input images turned out to be a different beast from predicting symbols in a full equation. To represent full equations, I concatenated several individual characters together to form a string of symbols -- for example, to form the equation "Ax+By=C", I would concatenate sample images from character classes in the sequence "A","x","+","B","y","=","C". This was a convenient trick that allowed me to simplify the training process, but also probably reduced the real-world accuracy of the model on actual handwritten equations.

The three test equations I used to validate the model are shown in the Carousel, each increasing in length and character complexity as they go. The model proved to be 96.43% accurate when used to predict the characters in these equations. 

## Text-to-LaTex Conversion
The second functional objective of the project was to create a conversion algorithm that would intake the output character strings of the ML model and convert them into their corresponding LaTex representation -- for example, the symbol ∑ would be represented as $\𝑠𝑢𝑚( )$. 

To develop this functionality, I built upon an existing python package "py2tex()" by coding in additional character symbols. The conversion process I devised was very similar to a dictionary look up in that the algorithm would compare the input character string with a library of possible symbols, match the symbol to it's LaTex representation, and then store it in the correct position in an output string that represents the LaTex equation. 

The final result was an accurate text-to-LaTex conversion algorithm. There were a few tricks I had to implement along the way to ensure the external py2tex package integrated nicely, and this explains why some extreneous parenthesis are present in the output LaTex equaitons.

## Documents

* [Final Project Report](/projects/OCR/OCRreport.pdf): Final project report with in-depth descriptions of machine learning principles
* [Final Project Presentation](https://youtu.be/qYKzP_sEDkw): Final presentation of project results
