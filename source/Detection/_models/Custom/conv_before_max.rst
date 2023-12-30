CustomYoloModel.add_conv_layer_before_maxpool
++++++++++++++++++++++++++++++++++++++++++++++++

.. method:: CustomYoloModel.add_conv_layer_before_maxpool(kernel_size, out_channels, stride, target_maxpool, padding=None)

    Adds a convolutional layer before a MaxPool layer in the architecture.

    :param kernel_size: The size of the kernel. Must be an odd number.
    :type kernel_size: int
    :param out_channels: The number of output channels.
    :type out_channels: int
    :param stride: The stride of the convolution.
    :type stride: int
    :param target_maxpool: The index of the MaxPool layer before which to add the convolutional layer.
    :type target_maxpool: int
    :param padding: The padding of the convolution. Default is (kernel_size-1) // 2.
    :type padding: int, optional

    :raises IndexError: If the index is out of range.