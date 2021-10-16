# imageseg
download mask rcnn
```
wget https://github.com/matterport/Mask_RCNN/releases/download/v1.0/mask_rcnn_coco.h5
```
#### 2. To convert keras model (h5) to tlite model, using the following code in colab
```
import tensorflow as tf

converter = tf.compat.v1.lite.TFLiteConverter.from_keras_model_file('mask_rcnn_coco.h5') 
tfmodel = converter.convert() 
open ('mask_rcnn_coco.tflite' , "wb") .write(tfmodel)
```

#### 3. To get tlite model to edgeTPU tlite model, you can use google colab by uploading the converted tlite model
https://colab.research.google.com/github/google-coral/tutorials/blob/master/compile_for_edgetpu.ipynb
