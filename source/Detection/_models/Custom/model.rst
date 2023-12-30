CustomYoloModel
+++++++++++++++++

.. class:: CustomYoloModel(in_channels=3, architecture=None, img_size=448, activation='LeakyReLU', **kwargs)

    A class that represents a custom `YOLO (You Only Look Once) <https://arxiv.org/abs/1506.02640>`_ model.

    This class is a subclass of the PyTorch nn.Module class. An instance of this class 
    represents a YOLO model, which is a type of Convolutional Neural Network (CNN) used 
    for object detection tasks.

    :param in_channels: Number of input channels. Default is 3.
    :type in_channels: int, optional
    :param architecture: The architecture of the CNN. Each element in the list represents a layer in the network. Default is an empty list.
    :type architecture: list, optional
    :param img_size: The size of the input images. Default is 448.
    :type img_size: int, optional
    :param activation: The type of activation function to use. Default is 'LeakyReLU'.
    :type activation: str, optional
    :param kwargs: Arbitrary keyword arguments for the fully connected layers.
    :type kwargs: dict, optional

    :ivar architecture: The architecture of the CNN. Each element in the list represents a layer in the network.
    :vartype architecture: list
    :ivar in_channels: Number of input channels.
    :vartype in_channels: int
    :ivar out_channels: Number of output channels.
    :vartype out_channels: int
    :ivar stride: The stride of the convolution.
    :vartype stride: int
    :ivar split_size: The size of the split.
    :vartype split_size: int
    :ivar img_size: The size of the input images.
    :vartype img_size: int
    :ivar activation: The type of activation function to use.
    :vartype activation: str
    :ivar darknet: The Darknet part of the YOLO model, which is a type of CNN.
    :vartype darknet: nn.Module
    :ivar fcs: The fully connected layers of the model.
    :vartype fcs: nn.Module

    * `add_conv_layer <add_conv.html>`_: This method allows users to add a convolutional layer to the architecture with the specified parameters (kernel size, number of output channnels, stride, padding).

    * `add_maxpool_layer <add_max.html>`_: This method allows users to add a max pooling layer to the architecture.

    * `add_dense_block <add_dense.html>`_: This method adds a dense block to the architecture. A dense block consists of two convolutional layers that are repeated a certain number of times.

    * `remove_last_layer <remove_last.html>`_: This method removes the last layer from the architecture.

    * `remove_last_n_layers <remove_last_n_layers.html>`_: This method removes the last n layers from the architecture.

    * `remove_all_layers <remove_all.html>`_: This method removes all layers from the architecture.

    * `modify_layer <modify.html>`_: This method modifies the specified layer in the architecture.

    * `add_conv_layer_before_maxpool <conv_before_max.html>`_: This method adds a convolutional layer before a max pooling layer in the architecture.

    * `validate_architecture <validate.html>`_: This method validates the model architecture to ensure it is potentially effective.

    .. note::
        Once the chosen architecture is validated, it is possible to train the model using our `train_Custom_model <train.html>`_ function. This function takes care of the entire training process, including loading the data, setting up the training loop, and saving the trained model.