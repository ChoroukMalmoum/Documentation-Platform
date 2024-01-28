CustomYoloModel.add_dense_block
+++++++++++++++++++++++++++++++++


.. method:: CustomYoloModel.add_dense_block(conv1, conv2, num_repeats)

    Adds a dense block to the architecture. A dense block consists of two convolutional layers that are repeated a certain number of times.

    :param conv1: The parameters of the first convolutional layer in the dense block.
    :type conv1: tuple
    :param conv2: The parameters of the second convolutional layer in the dense block.
    :type conv2: tuple
    :param num_repeats: The number of times the dense block is repeated.
    :type num_repeats: int