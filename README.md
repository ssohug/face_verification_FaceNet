# Face-is-the-Key

### Description
Face verification using OpenCV with FaceNet.



### Usage
**Create Database**

Store a few images of the user in ./dataset/user folder
```
cd dataset
cd user
```

Store a few images of random people in ./dataset/unknown folder
```
cd ..
cd unknown
```

**Create Embeddings**
To create embeddings for the user, run the following command - 
```
python extract_embeddings.py
```
This will store the embeddings in the pickle folder

**Train Classification Model** 
To train the SVM classification model, run the following command - 
```
python train_model.py
```


```
The face of the user will be recognized using the webcam.

### References 
1. <https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/>
2. <https://arxiv.org/abs/1503.03832>
3. <https://github.com/deepinsight/insightface>
4. <https://github.com/cmusatyalab/openface>
5. <https://www.youtube.com/watch?v=UB2VX4vNUa0>
6. <https://arxiv.org/abs/1910.04985>
