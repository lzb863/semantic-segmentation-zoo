# Usage

The only thing you have to do to get started is set up the folders in the following structure:

    ├── "dataset_name"                   
    |   ├── train
    |   ├── train_labels
    |   ├── val
    |   ├── val_labels
    |   ├── test
    |   ├── test_labels

Put a text file under the dataset directory called "class_dict.csv" which contains the list of classes along with the R, G, B colour labels to visualize the segmentation results. This kind of dictionairy is usually supplied with the dataset. Here is an example for the CamVid dataset:

```
name,r,g,b
Animal,64,128,64
Archway,192,0,128
Bicyclist,0,128, 192
Bridge,0, 128, 64
Building,128, 0, 0
Car,64, 0, 128
CartLuggagePram,64, 0, 192
Child,192, 128, 64
Column_Pole,192, 192, 128
Fence,64, 64, 128
LaneMkgsDriv,128, 0, 192
LaneMkgsNonDriv,192, 0, 64
Misc_Text,128, 128, 64
MotorcycleScooter,192, 0, 192
OtherMoving,128, 64, 64
ParkingBlock,64, 192, 128
Pedestrian,64, 64, 0
Road,128, 64, 128
RoadShoulder,128, 128, 192
Sidewalk,0, 0, 192
SignSymbol,192, 128, 128
Sky,128, 128, 128
SUVPickupTruck,64, 128,192
TrafficCone,0, 0, 64
TrafficLight,0, 64, 64
Train,192, 64, 128
Tree,128, 128, 0
Truck_Bus,192, 128, 192
Tunnel,64, 0, 64
VegetationMisc,192, 192, 0
Void,0, 0, 0
Wall,64, 192, 0
```

**Note:** If you are using any of the networks that rely on a pre-trained ResNet, then you will need to download the pre-trained weights using the provided script. These are currently: PSPNet, RefineNet, DeepLabV3, DeepLabV3+, GCN.

Then you can simply run `train.py`! Check out the optional command line arguments:

```
usage: train.py [-h] [--num_epochs NUM_EPOCHS]
                [--checkpoint_step CHECKPOINT_STEP]
                [--validation_step VALIDATION_STEP] [--image IMAGE]
                [--continue_training CONTINUE_TRAINING] [--dataset DATASET]
                [--crop_height CROP_HEIGHT] [--crop_width CROP_WIDTH]
                [--batch_size BATCH_SIZE] [--num_val_images NUM_VAL_IMAGES]
                [--h_flip H_FLIP] [--v_flip V_FLIP] [--brightness BRIGHTNESS]
                [--rotation ROTATION] [--model MODEL] [--frontend FRONTEND]

optional arguments:
  -h, --help            show this help message and exit
  --num_epochs NUM_EPOCHS
                        Number of epochs to train for
  --checkpoint_step CHECKPOINT_STEP
                        How often to save checkpoints (epochs)
  --validation_step VALIDATION_STEP
                        How often to perform validation (epochs)
  --image IMAGE         The image you want to predict on. Only valid in
                        "predict" mode.
  --continue_training CONTINUE_TRAINING
                        Whether to continue training from a checkpoint
  --dataset DATASET     Dataset you are using.
  --crop_height CROP_HEIGHT
                        Height of cropped input image to network
  --crop_width CROP_WIDTH
                        Width of cropped input image to network
  --batch_size BATCH_SIZE
                        Number of images in each batch
  --num_val_images NUM_VAL_IMAGES
                        The number of images to used for validations
  --h_flip H_FLIP       Whether to randomly flip the image horizontally for
                        data augmentation
  --v_flip V_FLIP       Whether to randomly flip the image vertically for data
                        augmentation
  --brightness BRIGHTNESS
                        Whether to randomly change the image brightness for
                        data augmentation. Specifies the max bightness change
                        as a factor between 0.0 and 1.0. For example, 0.1
                        represents a max brightness change of 10% (+-).
  --rotation ROTATION   Whether to randomly rotate the image for data
                        augmentation. Specifies the max rotation angle in
                        degrees.
  --model MODEL         The model you are using. See model_builder.py for
                        supported models
  --frontend FRONTEND   The frontend you are using. See frontend_builder.py
                        for supported models

```
