.. _model_selection:

Model
==========

Introduction
------------

The Model section of the platform allows users to choose the model they want to train for object detection and train it on their `own data <../Data\ Processing/user.html>`_. They have the following options:

1. YOLOv8: A popular object detection model.
2. TensorFlow Model Zoo: A collection of pre-trained object detection models provided by TensorFlow.
3. Custom Model: Users can construct their own object detection model based on YOLO configuration.

YOLOv8
------

`YOLOv8 <https://docs.ultralytics.com/>`_, the latest offering from `Ultralytics <https://www.ultralytics.com/>`_, is a top-tier model that builds upon the YOLO (You Only Look Once) architecture to enhance the capabilities of its predecessors. 
It introduces innovative features that improve performance, flexibility, and efficiency, and supports a wide range of vision AI tasks, including detection, segmentation, pose estimation, tracking, and classification. 
Thanks to its versatility, YOLOv8 serves as a valuable tool for various applications.

Users can use YOLOv8 directly from the platform to train it on their own dataset. 
The platform provides a simple interface that allows you to easily configure the model parameters and train the model using the provided dataset.
See the `Tutorial`_ for more details on how to train YOLOv8 on the platform.

For those preferring a code-based approach, the `YoloModel <yolov8/yolov8model.html>`_ class provides a way to harness the power of YOLOv8. 
This class offers a straightforward API to configure model parameters and train it on your dataset. 
It also facilitates inference using the trained model and model export.

The class includes the following key methods:

- `train <yolov8/trainyolov8.html>`_: Trains the model on the dataset and can resume training from a checkpoint.

- `predict_on_image <yolov8/predict_on_image.html>`_: Performs inference on a single image.

- `predict_on_video <yolov8/predict_on_video.html>`_: Executes inference on a video.

- `export <yolov8/exportyolov8.html>`_: Exports the trained model.

TensorFlow Model Zoo
--------------------

The `TensorFlow Model Zoo <https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md>`_ is a collection of pre-trained object detection models that can be used for various tasks.
These models, trained on the comprehensive COCO 2017 dataset, are ready for immediate inference tasks, especially if users categories of interest align with those in the COCO dataset.

However, the real power of these models is unleashed when they are used as a starting point for training on their own unique datasets. Our platform allows you to select one of these pre-trained models, initialize it with the pre-trained weights, and then train it on their dataset. This can potentially improve the model's performance and reduce training time.

To directly use a model from the TensorFlow Model Zoo for training on your own dataset, see the `Tutorial`_ for detailed instructions.

The `TensorflowModels <Tensorflow/tfmodels.html>`_ class provides a code-based approach to using these models. This class allows you to easily configure the model parameters and train it on your dataset. It also facilitates inference using the trained model and model export.

The class includes the following key methods:

- `download_model <Tensorflow/download_model.html>`_: Downloads the model from the TensorFlow Model Zoo if url is provided.

- `create_label_map <Tensorflow/labelmap.html>`_: Creates a label map for the dataset.
    .. note::
        A label map is a text file that maps each of the used labels to an integer value. This file is used to map the labels to indices, which are then used to construct the ground truth and prediction tensors.

- `data_to_tfrecord <Tensorflow/tfrecords.html>`_: Converts the dataset to `TFRecord format <https://www.tensorflow.org/tutorials/load_data/tfrecord>`_.
    .. note::
        TFRecord is the format required by TensorFlow Object Detection API for training.

- `get_model_type <Tensorflow/modeltype.html>`_: Returns the model type based on the configuration of the model. This can be used to modify the configuration of the model.

- `update_config_basic <TensorFlow/config.html>_`: Updates the configuration of the model based on the provided parameters.

- `train <Tensorflow/train.html>`_: Trains the model on the dataset.

- `evaluate <Tensorflow/eval.html>`_: Evaluates the model's performance on the dataset.

In order to test the model, we provide two functions that can be used to perform inference on images and webcam videos:

- `test_model_on_image <Tensorflow/testimage.html>`_: Performs inference on a single image.

- `test_model_on_camera <Tensorflow/testvideo.html>`_: Executes inference on a webcam.



Custom Model
------------

Our platform empowers users to construct their own object detection models, leveraging the `YOLO (You Only Look Once) <https://arxiv.org/abs/1506.02640>`_ configuration as a foundation. This provides users with the flexibility to customize the model architecture and training process according to their specific requirements.

The platform assists users in creating their models by allowing them to add layers (such as convolutional layers, max pooling layers, etc.) and choose options as per their needs. It also validates the architecture to ensure that the created model has the potential to perform effectively.

To directly construct a custom model from the platform, follow the instructions in the `Tutorial`_.

The `CustomYoloModel <Custom/model.html>`_ class allows users to create their own object detection model. This class includes the following methods:

- `add_conv_layer <Custom/add_conv.html>`_: This method allows users to add a convolutional layer to the architecture with the specified parameters (kernel size, number of output channnels, stride, padding).

- `add_maxpool_layer <Custom/add_max.html>`_: This method allows users to add a max pooling layer to the architecture.

- `add_dense_block <Custom/add_dense.html>`_: This method adds a dense block to the architecture. A dense block consists of two convolutional layers that are repeated a certain number of times.

- `remove_last_layer <Custom/remove_last.html>`_: This method removes the last layer from the architecture.

- `remove_last_n_layers <Custom/remove_last_n_layers.html>`_: This method removes the last n layers from the architecture.

- `remove_all_layers <Custom/remove_all.html>`_: This method removes all layers from the architecture.

- `modify_layer <Custom/modify.html>`_: This method modifies the specified layer in the architecture.

- `add_conv_layer_before_maxpool <Custom/conv_before_max.html>`_: This method adds a convolutional layer before a max pooling layer in the architecture.

- `validate_architecture <Custom/validate.html>`_: This method validates the model architecture to ensure it is potentially effective.


The `train_Custom_model <Custom/train.html>`_ function can be used to train the model once the chosen architecture is validated. This function takes care of the entire training process, including loading the data, setting up the training loop, and saving the trained model.


Conclusion
----------

The user model section of the platform provides users with the flexibility to choose the object detection model that best suits their needs. Whether they prefer YOLOv8, a model from the TensorFlow Model Zoo, or a custom model, they can easily train and deploy their chosen model using the platform's features.

.. note::
    For detailed instructions on using each model option, refer to the respective documentation sections.
