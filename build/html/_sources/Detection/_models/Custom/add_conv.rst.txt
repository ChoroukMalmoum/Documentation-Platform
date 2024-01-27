CustomYoloModel.add_conv_layer
+++++++++++++++++++++++++++++++

.. method:: CustomYoloModel.add_conv_layer(kernel_size, out_channels, stride, padding=None)

    Adds a convolutional layer to the architecture.

    :param kernel_size: The size of the kernel. Must be an odd number.
    :type kernel_size: int
    :param out_channels: The number of output channels.
    :type out_channels: int
    :param stride: The stride of the convolution.
    :type stride: int
    :param padding: The padding of the convolution. Default is (kernel_size-1) // 2.
    :type padding: int, optional