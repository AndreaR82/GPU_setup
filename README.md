# GPU_setup

Steps to install TF with GPU capabilities and be able to run convnets on GPU in Python (at least).

1. Install GPU drivers (418 with CUDA 10.1)
2. Install conda
3. Create environment with keras-gpu which will install all dependencies, including TF 2.1
4. Add the following snippet at the beginning of the Python script:

```{python}
import tensorflow as tf
config = tf.compat.v1.ConfigProto()
config.gpu_options.allow_growth = True
session = tf.compat.v1.InteractiveSession(config=config)
```
