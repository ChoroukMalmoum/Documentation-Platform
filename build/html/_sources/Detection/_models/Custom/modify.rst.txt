CustomYoloModel.modify_layer
+++++++++++++++++++++++++++++

.. method:: CustomYoloModel.modify_layer(index, new_params)

    Modifies a layer in the architecture.

    :param index: The index of the layer to modify.
    :type index: int
    :param new_params: The new parameters of the layer.
    :type new_params: tuple

    :raises IndexError: If the index is out of range.