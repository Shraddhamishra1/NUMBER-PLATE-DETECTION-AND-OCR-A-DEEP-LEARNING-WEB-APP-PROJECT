# NUMBER PLATE DETECTION AND OCR: A DEEP LEARNING WEB APP PROJECT

Deep Learning project to identify number plate positions and character recognition.Using the Object Detection model, image which contains the license plate are cropped which is also called the region of interest(ROI), and pass the ROI to Optical Character Recognition API Tesseract in Python (Pytesseract). 
This model,is used to extract text from image.Deep Learning model pipeline is build by putting all together.


## Dependencies

    1) Tensorflow
    2) Sklearn
    3) Pandas
    4) OpenCV
    5) Numpy
    6) Matplotlib
    7) HTML
    8) Bootstrap
    9) Flask
    10) OS





## Installation

* Install image Annotation Tool https://github.com/tzutalin/labelImg

* LabelImg is a graphical image annotation tool. 
* Annotations are saved as XML files in PASCAL VOC format, the format used by ImageNet. Besides, it also supports YOLO and CreateML formats.

## Labelling    
### Windows

* Install Python, PyQt5 and install lxml.
* Open cmd and go to the labelImg directory
```bash
pyrcc4 -o libs/resources.py resources.qrc
For pyqt5, pyrcc5 -o libs/resources.py resources.qrc
python labelImg.py
python labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
```
* Open folder with images in labelImg software and create box around number plate label it and save the image
## Data Preprocessing
* Converting labelled images to array using Tensorflow keras, get normalized values of labels

## Deep Learning Model
### Trainning
* This deep learning object detection model is trained using InceptionResnet V2 in TensorFlow 2. 
* Provide path of object detection folder to Tensorboard to complete trainning Preprocessing
* Save model to models folder in same directory
### Predictions
* Load model saved in ```./models/object_detection.h5``` in keras models
* Load image and convert it into array and get normalized output
* Values are denormalized to get original values of coordinates
## Optical Character recognition

### Tesseract

Tesseract is open source optical character software that is used to extract test from image

* Install Tesseract 
```
https://osdn.net/projects/sfnet_tesseract-ocr-alt/downloads/tesseract-ocr-setup-3.02.02/
```


* Install Pytesseract an python API 
```
pip install --upgrade pytesseract
```

## Flask App

* Download and install Visual studio code
* Install Flask
``` 
pip install flask
```
* Run App 
```
python app.py
```
