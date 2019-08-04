# Contributing to Semantic Segmentation Zoo


All pull requests which improve the code or add new features are welcome! 

This repository is forked from [Semantic-Segmentation-Suite](https://github.com/GeorgeSeif/Semantic-Segmentation-Suite) since it has been deprecated.


## Rules

* Try to follow the same style as the code base.
* Supports python 3 as a minimum.
* Should not break anything.
* If you are contributing a new network from a paper, make sure you test it with all of the frontends (ResNet, Inception, MobileNet). It's alright if it doesn't work with a couple of them, just be sure to report it and note it down.
* Make sure your new code doesn't break anything. Test it thoroughly.
* It is recommended that the first line of the commit message should not exceed 72 characters.


## Files and Directories

* **train.py:** Training on the dataset of your choice. Default is CamVid.
* **test.py:** Testing on the dataset of your choice. Default is CamVid.
* **predict.py:** Use your newly trained model to run a prediction on a single image.
* **helper.py:** Quick helper functions for data preparation and visualization
* **utils.py:** Utilities for printing, debugging, testing, and evaluation.
* **models:** Folder containing all model files. Use this to build your models, or use a pre-built one.
* **CamVid:** The CamVid datatset for Semantic Segmentation as a test bed. This is the 32 class version.
* **checkpoints:** Checkpoint files for each epoch during training.
* **Test:** Test results including images, per-class accuracies, precision, recall, and f1 score.
