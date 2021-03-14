# Tensorflow_Cheatsheet
## Epochs Callback Function
Stops the epochs after the epoch reach a curtain accuracy
accuracy should be a float <= 1
```py
class myCallback(tf.keras.callbacks.Callback):
      def on_epoch_end(self, epoch, logs={}, acc=1):
        if(logs.get('accuracy') and logs.get('accuracy')>acc):
          print(f"\nReached {acc*100}% accuracy so cancelling training!")
          self.model.stop_training = True

callback = myCallback(accuracy)
```
