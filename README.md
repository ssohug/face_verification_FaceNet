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
python3 extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7
```
This will store the embeddings in the pickle folder

**Train Classification Model** 
To train the SVM classification model, run the following command - 
```
python3 train_model.py --embeddings output/embeddings.pickle     --recognizer output/recognizer.pickle   --le output/le.pickle
```



To verify the face run the following command -
```
python3 recognize.py --detector face_detection_model     --embedding-model openface_nn4.small2.v1.t7     --recognizer output/recognizer.pickle   --le output/le.pickle   --image images/aii.png
```
### References 
1. <https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/>
2. <https://arxiv.org/abs/1503.03832>
3. <https://github.com/deepinsight/insightface>
4. <https://github.com/cmusatyalab/openface>
5. <https://www.youtube.com/watch?v=UB2VX4vNUa0>
6. <https://arxiv.org/abs/1910.04985>
