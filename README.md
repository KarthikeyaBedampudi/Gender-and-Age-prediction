# 🧑‍💻 Gender and Age Detection with OpenCV DNN

This project uses **OpenCV's deep learning module (DNN)** to detect faces in images and predict the **gender** and **age group** of each detected face using pre-trained Caffe models.

---

## 📸 Example Output

The program annotates each detected face with predictions like:

```
Female, 25-32
Male, 15-20
```

---

## 🧠 How It Works

The system works in 3 stages:

1. **Face Detection**

   * Uses OpenCV’s pre-trained face detector (`opencv_face_detector_uint8.pb`)

2. **Gender Prediction**

   * Uses `gender_net.caffemodel` to classify face as either **Male** or **Female**

3. **Age Estimation**

   * Uses `age_net.caffemodel` to classify the face into one of 8 age ranges

---

## 🧾 Age Groups

```
['(0-2)', '(4-6)', '(8-12)', '(15-20)', '(25-32)', '(38-43)', '(48-53)', '(60-100)']
```

## ⚙️ Folder Structure

```
project/
├── models/
│   ├── opencv_face_detector.pbtxt
│   ├── opencv_face_detector_uint8.pb
│   ├── age_deploy.prototxt
│   ├── age_net.caffemodel
│   ├── gender_deploy.prototxt
│   ├── gender_net.caffemodel
├── images/
│   ├── person1.jpg
│   └── person2.jpg
├── detect_gender_age.py
└── README.md
```

---

## 🛠 Requirements

Install dependencies:

```bash
pip install opencv-python numpy
```

---

## 🚀 How to Run

Place your images in the `images/` folder.

Then run:

```bash
python detect_gender_age.py
```

The program will:

* Loop through all images in the folder
* Detect faces
* Annotate each face with predicted gender and age
* Display each result one at a time

---

## 🧪 Example Use Cases

* Demographic analysis
* Audience profiling for smart signage
* Interactive kiosks and mirrors
* Just for fun!

---


## 📚 Credits

* Pre-trained models by [Levi & Hassner](https://talhassner.github.io/home/projects/Adience/)
* OpenCV DNN face detector

---
