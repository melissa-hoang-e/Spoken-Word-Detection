# Spoken Word Detection System

Spoken word detection is a crucial task in various practical applications, including voice assistants, transcription services, and audio content analysis. This project aims to develop an efficient and adaptable spoken word detection system that focuses on robustness to noise and speaker variability while leveraging state-of-the-art machine learning and speech processing techniques.

## Table of Contents
- [Introduction](#introduction)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Training Procedure](#training-procedure)
- [Evaluation](#evaluation)
- [Discussion](#discussion)
- [Conclusion](#conclusion)

## Introduction

The field of machine learning has witnessed significant advancements in recent years, revolutionizing various domains and applications. One area that has garnered substantial attention is the detection of spoken words, which plays a crucial role in numerous applications such as speech recognition, natural language processing, and audio analysis. This project aims to develop a speech command classification system by leveraging state-of-the-art machine learning techniques.

## Model Architecture

The M5 model is a deep learning architecture specifically designed for speech command classification tasks. It is a modified version of the original M5 model introduced in the webpage "Convolutional Neural Networks for Small-footprint Keyword Spotting" by Sainath et al [8]. The model employs convolutional layers with batch normalization, max pooling, and fully connected layers. This design allows the model to automatically learn discriminative features and temporal patterns from audio data.

## Dataset

The dataset used in this project is the Speech Commands dataset from Google, which is commonly used for speech command classification tasks. It consists of spoken commands from various individuals, recorded in different environments. The dataset includes a diverse set of commands such as "yes," "no," "up," "down," and many others. Each data point contains information about its waveform, sample rate, label, speaker ID, and utterance number. Data preprocessing steps include resampling, Mel Frequency Cepstral Coefficients (MFCC) transformation, and normalization to make the features suitable for training the neural network.

## Training Procedure

The training is conducted using Google Colab to take advantage of pre-installed libraries and GPU resources. The optimizer used is Adam, with a specified learning rate and weight decay. A StepLR scheduler is employed to decrease the learning rate after a set number of epochs. Early stopping with a patience of 10 is applied to prevent overfitting. The training process involves both training and validation phases, with the best model saved for future use.

## Evaluation

The model's performance is evaluated on the test dataset using accuracy as the evaluation metric. A confusion matrix is plotted to gain insights into how well the model is performing for each class and identify specific misclassifications. The test accuracy achieved is 75%, indicating the model's suitability for various applications.

## Discussion

The training terminated early, suggesting that the model may have reached its capacity with the given data. Further model improvements can be explored by increasing model complexity or using more advanced architectures with transfer learning. Additionally, data augmentation techniques, such as adding background noise and time stretching, can be considered to enhance the model's robustness in different environmental conditions.

## Conclusion

In conclusion, this project successfully develops a speech recognition system using a CNN trained on the Speech Commands dataset. The trained model demonstrates a satisfactory level of accuracy, making it effective for classifying speech commands. Data preprocessing techniques, including MFCC extraction and normalization, play a crucial role in preparing the input data for the CNN model. With further improvements and adaptations, the model can find applications in voice-controlled interfaces and other practical domains.
