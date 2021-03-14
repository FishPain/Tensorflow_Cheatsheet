# Tensorflow_Cheatsheet
```py
class myCallback(tf.keras.callbacks.Callback):
      def on_epoch_end(self, epoch, logs={}):
        if(logs.get('accuracy') and logs.get('accuracy')>0.998):
          print("\nReached 99.8% accuracy so cancelling training!")
          self.model.stop_training = True
    callback = myCallback()
```
