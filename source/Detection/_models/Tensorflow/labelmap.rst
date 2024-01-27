TensorflowModels.create_label_map
++++++++++++++++++++++++++++++++++++++

.. method:: TensorflowModels.create_label_map()

    Creates a label map for the classes.

    This method writes the classes from the dataset 
    to the 'LABELMAP' file in the format required by TensorFlow. If the 'LABELMAP' 
    file already exists, it is overwritten.

    :raises FileNotFoundError: If the 'CLASSES_TXT' file does not exist.
    :raises IOError: If there is an error during the reading or writing of the files.

    .. note::
        A label map is a text file that maps each of the used labels to an integer value. This file is used to map the labels to indices, which are then used to construct the ground truth and prediction tensors.
