# Coursework for the 'Computer Vision' course

## Motivation
For this work I wanted to learn to track and detect objects on a video. So I choosed to focus on detecting vehicles as a start point.
And as realization I was inspired by YOLO model.

## Dataset

There are few datasets on the internet, like: VSAI, COWC, DOTA, FAIR1M and others.
The problem with some of them: not enough images for training the model, or images made by Satellite (with very small vehicles on the image), not clear classification or little number of vehicle classes.

I chose to work with [Vehicle Detection in Aerial Imagery (VEDAI) dataset](https://downloads.greyc.fr/vedai/) found at Roboflow Universe resource. 
Dataset was initially created by Sebastien Razakarivony and Frederic Jurie in 2014. 

There is [Roboflow collection](https://universe.roboflow.com/ntokozo-nhlangothi-w6os9/vedai-roboflow/dataset/1) (v1) as well, that was prepared specifically for YOLOv8.

Datase contains 5288 images in total as a JPEG file of size 640x640 pixels.

Dataset contains following classes: plane, boat, camping car, car, pick-up, tractor, truck, van, and other.

## Prerequisites
I recommend to use Google Colab to run the code, since it allows to use GPU for faster calculations. And to be able to work with Google Colab you must have Gmail account.

## How to work with this project
1. Clone this repo to your local machine
2. Go to https://colab.research.google.com/
3. There, in a popup dialog, choose to Upload Jupyter Notebook to Google Colab. Open notebook.
4. Before running notebook you will need dataset. Download dataset from Roboflow [here](https://universe.roboflow.com/ntokozo-nhlangothi-w6os9/vedai-roboflow/dataset/1). Un-zip it.
5. Upload all files and folders as it is to Google Drive. (There is code in notebook for accessing Google Drive from Google Colab. Provide access).
6. Run code in notebook gradually. Before fine-tuning the model, in Colab settings set to use GPU


## What results

Fine-tuned (trained on custom dataset) model works good on test dataset.
But testing prediction on video file didn't work.

## What's next?

- Make it work on video files
- Maybe try other datasets available on Internet
- Find Satellite images with different vehicles and, using Roboflow or other tool, create annotations with custom classes
- Try other YOLO models. Compare results
- Try with images made at night or on a cloudy day
