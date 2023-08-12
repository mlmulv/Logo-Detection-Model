<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#authors">Authors</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project consists of using a Convolutional Neural Network (CNN) to accomplish logo classification. We are given 10 different logos and the model will classify what brand the image belongs to. 

![Screenshot](https://github.com/UF-FundMachineLearning-Summer23/final-project---code-report-artificial-unintelligence/blob/main/brand_table.png)

Note: Gator corresponds to UF Gator Logo

<!-- GETTING STARTED -->
## Getting Started

### Dependencies

Our code was implemented on a Tensorflow-2.7.0 kernel provided by University of Florida HiPerGator,therefore we did not have to install our own dependicies. I will include what versions we used if you would like to add into your conda environment.

* numpy 1.22.3
  ```sh
  conda install -c conda-forge numpy
  ```
    
* opencv-python 4.5.5
  ```sh
  conda install -c conda-forge opencv
  ```
  
* scikit-learn 0.42.2
  ```sh
  conda install -c conda-forge scikit-learn
  ```
  
 * tensorflow 2.7.0
   ```sh
   conda install -c conda-forge tensorflow
   ```
### Installation

*  Clone the repo
   ```sh
   git clone https://github.com/mlmulv/Logo-Detection-Model
   ```

<!-- USAGE EXAMPLES -->
## Usage

1. Training model
    * A. The notebook **train.ipynb** will contain the **train function**.
    * B. The train function has two inputs:
         1. data_train - a .npy file type that is shape (270000,# of photos). 270,000 corresponds the amount of pixels for a flattened 300x300 RGB image.
         2. labels_train - a .npy file that contains labels that are integer encoded for each image.
    * C. When the model is training you can see the performance metrics during each epoch.
    * D. When the model has finished completing, it will save the model to your directory as a .h5 file.
    
2. Testing model
   *  A. The notebook **test.ipynb** will contain the **test function**.
    * B. You will need to input your own model with .h5 filetype
    * C. There are two types of data sets that you can input:
         1. An "easy" dataset that will consist of images with classes that have been seen by the model
         2. A "hard" dataset that will consist of images that may have classes not seen by the model
   *  D. Labels from easy dataset will consist of the same integer encoded labels. While labels from the harder dataset will consist of a label of [-1] for classes than have not been seen by the model.
    * E. To test with an "easy" dataset you will enter a "0" for the difficulty input, and to test with a "hard" datset you will enter a "1".
    * F. Model will output accuracy of predicted labels compared to given labels, and a numpy array of the predicted labels.
    * G. If you would like to use my trained model for testing you can use the **logo_classification_model.h5** to do so.



<!-- Authors -->
## Authors

Markus Mulvihill - [LinkedIn](https://www.linkedin.com/in/markus-mulvihill-6549961a0/) - markusmulvihill1103@gmail.com

Project Link: (https://github.com/mlmulv/Logo-Detection-Model)


