utils.test_model_on_camera
++++++++++++++++++++++++++++


.. function:: utils.test_model_on_camera(model)

    Tests the given TensorFlow model on a video stream from the default camera.

    This function captures video from the default camera, runs each frame through the model,
    and visualizes the detection results on the frame. The detections are visualized
    using the `visualize_boxes_and_labels_on_image_array` function from the TensorFlow
    Object Detection API's visualization utilities.

    The function continues to process frames until the 'q' key is pressed.

    :param model: The TensorFlow model to test.
    :type model: TensorFlow Model
    :raises RuntimeError: If the camera could not be opened or a frame could not be read.