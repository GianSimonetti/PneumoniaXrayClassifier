# PneumoniaXrayClassifier

This project develops an AI model to classify chest X-ray images for pneumonia detection. It uses deep learning techniques and is trained on a dataset of X-ray images. The goal is to train a model that can distinguish between X-rays of healthy patients and those with pneumonia.

The AI model is trained and evaluated using the Google Colab environment, with data stored in Google Drive. Prior to training, the folders containing the images are unzipped (code for this process is provided). All information is accessed from Google Drive for convenience. The code to mount the corresponding folders in Google Drive is also provided.

## Steps

### Data Loading
The X-ray images are classified into two categories: NORMAL and PNEUMONIA. Initially, the compressed images are decompressed and placed into 'Train' and 'Test' folders, respectively, using the provided code. The images are loaded from these specific directories, assigned labels based on whether they are in the NORMAL or PNEUMONIA category, and preprocessed by resizing them to a uniform size and converting them to grayscale. The processed data is saved in files to avoid constant reloading, stored in a new folder named 'StoredImages' to prevent unnecessary delays.

### Model Structure
A convolutional neural network (CNN) model is used, consisting of several convolutional and pooling layers. The model is compiled using the Adam optimizer and the sparse_categorical_crossentropy loss function.

### Training and Evaluation
The model is trained with the preprocessed images for 20 epochs. TensorBoard is used for monitoring the training process. The model's accuracy is evaluated on both the training and test data.
