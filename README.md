# Tensorflow_Cheatsheet
## Epochs Callback Function
```py
class myCallback(tf.keras.callbacks.Callback, accuracy=None):
      def on_epoch_end(self, epoch, logs={}):
        if(logs.get('accuracy') and logs.get('accuracy')>accuracy):
          print("\nReached 99.8% accuracy so cancelling training!")
          self.model.stop_training = True

callback = myCallback(accuracy=[A Float >= 1])
```
