utils.test_model_on_image
++++++++++++++++++++++++++


.. function:: utils.test_model_on_image(image_path, model)

    Tests the given TensorFlow model on an image and visualizes the detections.

    This function reads an image from the given path, runs it through the model,
    and visualizes the detection results on the image. The detections are visualized
    using the `visualize_boxes_and_labels_on_image_array` function from the TensorFlow
    Object Detection API's visualization utilities.

    :param image_path: The path to the image file to test the model on.
    :type image_path: str
    :param model: The TensorFlow model to test.
    :type model: TensorFlow Model
    :raises FileNotFoundError: If the image file does not exist.