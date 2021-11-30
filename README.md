## For Deep Learning



### Tensorflow

* Download tensorflow on mac m1:
```
1. create environment    ------> conda create -n tf tensorflow     (done)    
2. using tf on jupyter   ------>  conda activate tf
                                  conda install jupyter
                                  python -m ipykernel install --user --name=tf.   (done)
```
* Using Custom Callbacks: <br>
If training has to stop once accuracy reaches 60%,
```
class myCallback(tf.keras.callbacks.Callback):
  def on_epoch_end(self, epoch, logs={}):
    if(logs.get('acc')>0.6):
      print("\nReached 60% accuracy so cancelling training!")
      self.model.stop_training = True
      
callbacks = myCallback()

model.fit(x_train, y_train, epochs=10, callbacks=[callbacks])
```
* Uploading images to test the tf classification model: <br>
```
import numpy as np
from google.colab import files     # tested in Google Colab - find similar syntax for jupyter
from keras.preprocessing import image

uploaded = files.upload()

for fn in uploaded.keys():
 
  # predicting images
  path = '/content/' + fn        # path to store the uploaded image (from local)
  img = image.load_img(path, target_size=(300, 300)) # image converted to 300 x 300 pixels
  x = image.img_to_array(img)
  x = np.expand_dims(x, axis=0)

  images = np.vstack([x])
  classes = model.predict(images, batch_size=10) # trained moddel
  print(classes[0])
  if classes[0]>0.5:
    print(fn + " is a human")     # this is a binary classifier
  else:
    print(fn + " is a horse")
```
* Classification Metrics

| Metric | Formula | code | Comments
|-|-|-|-
| Accuracy | (tp+tn)/(tp+tn+fp+fn) | tf.keras.metrics.Accuracy()  | Default
| Precision | (tp)/(tp+fp) | tf.keras.metrics.Precision() | Less FP
| Recall | (tp)/(tp+fn) | tf.keras.metrics.Recall() | Less FN
| F1 Score | 2.(P . R)/(P+R) | sklearn | Overall
| Confusion Matrix | - | sklearn | Overall
