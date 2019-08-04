# Semantic Segmentation Zoo

<p align="center">
<img src="https://github.com/xxxnell/semantic-segmentation-zoo/blob/master/docs/semseg.gif" style="max-width: 500px; width: 100%;">
</p>

This repository provides various [models](docs/models.md) for semantic segmentation. The goal is to compare the various semantic segmentation models and make it easier to implement new model. Complete with the following:

* Training and testing modes
* Data augmentation
* Several state-of-the-art models. Easily plug and play with different models
* Able to use any dataset
* Evaluation including precision, recall, f1 score, average accuracy, per-class accuracy, and mean IoU
* Plotting of loss function and accuracy over epochs


## Getting Started

This project has the following dependencies:

* Numpy `sudo pip install numpy`
* OpenCV Python `sudo apt-get install python-opencv`
* TensorFlow `sudo pip install --upgrade tensorflow-gpu`

Then you can simply run `train.py`. Default dataset is [CamVid](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/). See [usage](docs/usage.md) documentation for more details.


## Contributing

Contributions are always welcome. Any kind of contribution, such as writing a unit test, documentation, bug fix, is helpful.

Fo more detail, see the [contributing](CONTRIBUTING.md) documentation.


## License

All code is available to you under the [Apache License 2.0](LICENSE).

Copyright the maintainers.


    