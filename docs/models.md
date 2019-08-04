# Models

The following segmentation models are currently made available:

- [Encoder-Decoder based on SegNet](https://arxiv.org/abs/1511.00561). This network uses a VGG-style encoder-decoder, where the upsampling in the decoder is done using transposed convolutions.

- [Encoder-Decoder with skip connections based on SegNet](https://arxiv.org/abs/1511.00561). This network uses a VGG-style encoder-decoder, where the upsampling in the decoder is done using transposed convolutions. In addition, it employs additive skip connections from the encoder to the decoder. 

- [Mobile UNet for Semantic Segmentation](https://arxiv.org/abs/1704.04861). Combining the ideas of MobileNets Depthwise Separable Convolutions with UNet to build a high speed, low parameter Semantic Segmentation model.

- [Pyramid Scene Parsing Network](https://arxiv.org/abs/1612.01105). In this paper, the capability of global context information by different-region based context aggregation is applied through a pyramid pooling module together with the proposed pyramid scene parsing network (PSPNet). **Note that the original PSPNet uses a ResNet with dilated convolutions, but the one is this respository has only a regular ResNet.**

- [The One Hundred Layers Tiramisu: Fully Convolutional DenseNets for Semantic Segmentation](https://arxiv.org/abs/1611.09326). Uses a downsampling-upsampling style encoder-decoder network. Each stage i.e between the pooling layers uses dense blocks. In addition, it concatenated skip connections from the encoder to the decoder. In the code, this is the FC-DenseNet model.

- [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1706.05587). This is the DeepLabV3 network. Uses Atrous Spatial Pyramid Pooling to capture multi-scale context by using multiple atrous rates. This creates a large receptive field. 

- [RefineNet: Multi-Path Refinement Networks for High-Resolution Semantic Segmentation](https://arxiv.org/abs/1611.06612). A multi-path refinement network that explicitly exploits all the information available along the down-sampling process to enable high-resolution prediction using long-range residual connections. In this way, the deeper layers that capture high-level semantic features can be directly refined using fine-grained features from earlier convolutions.

- [Full-Resolution Residual Networks for Semantic Segmentation in Street Scenes](https://arxiv.org/abs/1611.08323). Combines multi-scale context with pixel-level accuracy by using two processing streams within the network. The residual stream carries information at the full image resolution, enabling precise adherence to segment boundaries. The pooling stream undergoes a sequence of pooling operations to obtain robust features for recognition. The two streams are coupled at the full image resolution using residuals. In the code, this is the FRRN model.

- [Large Kernel Matters -- Improve Semantic Segmentation by Global Convolutional Network](https://arxiv.org/abs/1703.02719). Proposes a Global Convolutional Network to address both the classification and localization issues for the semantic segmentation. Uses large separable kernals to expand the receptive field, plus a boundary refinement block to further improve localization performance near boundaries. 

- [AdapNet: Adaptive Semantic Segmentation in Adverse Environmental Conditions](http://ais.informatik.uni-freiburg.de/publications/papers/valada17icra.pdf) Modifies the ResNet50 architecture by performing the lower resolution processing using a multi-scale strategy with atrous convolutions. This is a slightly modified version using bilinear upscaling instead of transposed convolutions as I found it gave better results.

- [ICNet for Real-Time Semantic Segmentation on High-Resolution Images](https://arxiv.org/abs/1704.08545). Proposes a compressed-PSPNet-based image cascade network (ICNet) that incorporates multi-resolution branches under proper label guidance to address this challenge. Most of the processing is done at low resolution for high speed and the multi-scale auxillary loss helps get an accurate model. **Note: I have implemented the network but have not integrated its training yet**

- [Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1802.02611). This is the DeepLabV3+ network which adds a Decoder module on top of the regular DeepLabV3 model.

- [DenseASPP for Semantic Segmentation in Street Scenes](http://openaccess.thecvf.com/content_cvpr_2018/html/Yang_DenseASPP_for_Semantic_CVPR_2018_paper.html). Combines many different scales using dilated convolution but with dense connections

- [Dense Decoder Shortcut Connections for Single-Pass Semantic Segmentation](http://openaccess.thecvf.com/content_cvpr_2018/html/Bilinski_Dense_Decoder_Shortcut_CVPR_2018_paper.html). Dense Decoder Shorcut Connections using dense connectivity in the decoder stage of the segmentation model. **Note: this network takes a bit of extra time to load due to the construction of the ResNeXt blocks** 

- [BiSeNet: Bilateral Segmentation Network for Real-time Semantic Segmentation](https://arxiv.org/abs/1808.00897). BiSeNet use a Spatial Path with a small stride to preserve the spatial information and generate high-resolution features while having a parallel Context Path with a fast downsampling strategy to obtain sufficient receptive field. 

- Or make your own and plug and play!


## Feature Extraction

The following feature extraction models are currently made available:

- [MobileNetV2](https://arxiv.org/abs/1801.04381), [ResNet50/101/152](https://arxiv.org/abs/1512.03385), and [InceptionV4](https://arxiv.org/abs/1602.07261)

