
# RealTime-Handwritten-Kannada-Character-Recognition

This project aims to perform real-time handwritten Kannada character recognition using computer vision and machine learning techniques. It allows users to draw Kannada characters in real-time using tools like Paint3D, and the system predicts the characters instantly.


## Overview

The project consists of two main Python files, each showcasing different aspects of the recognition system:

- digits+(a to aha).ipynb: This file contains the implementation for training and testing a recognition model on Kannada digits (0-9) and Kannada alphabets (ಅ to ಅಃ). Various machine learning algorithms such as SVM, KNN, and CNN are experimented with to achieve optimal performance.

- digits+(a to laa).ipynb: Similar to the first file, this one focuses on training and testing a recognition model on Kannada digits (0-9) and Kannada alphabets (ಅ to ಳ). It also explores different machine learning algorithms to compare performance with the previous dataset.

## Dataset

 
The dataset used in this project was prepared by me- Rumana Begum and my friends- Lakshmishree B U, Naveen Kumar H G and is available for download on Kaggle. You can access the dataset [by clicking here](https://www.kaggle.com/datasets/rumanabegum/handwritten-kannada-dataset). It consists of three zipped files:
- **captured_images**: Contains the raw handwritten Kannada character images.
- **kan_data**: Contains the dataset used for training and testing the recognition models with Kannada digits (0-9) and Kannada alphabets (ಅ to ಅಃ).
- **kannada_full_data**: Contains the dataset used for training and testing the recognition models with Kannada digits (0-9) and Kannada alphabets (ಅ to ಳ).
## Dependencies

This project relies on several Python libraries and tools, including:

- OpenCV (cv2)
- numpy
- pandas
- matplotlib
- scikit-learn
- TensorFlow (for CNN implementation)
- joblib
- pyscreenshot
- Paint3D (for drawing characters in real-time)
Ensure that these libraries are installed in your environment before running the project.
    
## Deployment

This script captures screenshots of a defined area on your computer screen every 4 seconds, saving them as image files in a folder

```bash
import pyscreenshot as ImageGrab
import time

def one_time():
    images_folder = "captured_images/oww/"
    
    # Capture and save images
    for i in range(0, 100):
        time.sleep(4)
        im = ImageGrab.grab(bbox=(60, 170, 400, 550))  # x1, y1, x2, y2
        print("saved......", i)
        im.save(images_folder + str(i) + '.png')
        print("clear screen now and redraw now........")
```


## Comparative Performance of Models
This project provides us with great insights about the various algorithms which could be used in classification problems and how it performs as the number of classes increases:
|              Classes                                             | SVM   | KNN   | CNN   |
|-----------------------------------------------------|-------|-------|-------|
| Kannada digits (0-9), Kannada alphabets (ಅ to  ಅಃ) | 85.26%  | 81.27%  | 93.63%  |
| Kannada digits (0-9), Kannada alphabets (ಅ to ಳ)   | 72.98%  | 70.05%  | 89.50%  |
