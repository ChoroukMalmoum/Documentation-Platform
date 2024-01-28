Augmenter
+++++++++++++++++++++++++++++++++

.. class:: Augmenter(image, label, augmentation_ids, rotaion_degrees=180, crop_size=50, shear=(-15, 15, -15, 15), shear_degress=1, hue=(-0.1, 0.1), saturation=(0, 3), brightness=(0, 3), gaussian_blur_kernel_size=15)

   Class for data augmentation on images and bounding boxes.

   :param image: BytesIO object containing image data.
   :type image: BytesIO
   :param label: BytesIO object containing label data.
   :type label: BytesIO
   :param augmentation_ids: List of indices representing augmentations to apply.
   :type augmentation_ids: list
   :param rotaion_degrees: Rotation degrees for RandomRotation. Defaults to 180.
   :type rotaion_degrees: int, optional
   :param crop_size: Size of the crop for RandomCrop. Defaults to 50.
   :type crop_size: int, optional
   :param shear: Shear range for RandomAffine. Defaults to (-15, 15, -15, 15).
   :type shear: tuple, optional
   :param shear_degress: Degrees for shear in RandomAffine. Defaults to 1.
   :type shear_degress: int, optional
   :param hue: Range of hue adjustment for ColorJitter. Defaults to (-0.1, 0.1).
   :type hue: tuple, optional
   :param saturation: Range of saturation adjustment for ColorJitter. Defaults to (0, 3).
   :type saturation: tuple, optional
   :param brightness: Range of brightness adjustment for ColorJitter. Defaults to (0, 3).
   :type brightness: tuple, optional
   :param gaussian_blur_kernel_size: Kernel size for GaussianBlur. Defaults to 15.
   :type gaussian_blur_kernel_size: int, optional

   * `augment <Augmenter-augment.html>`_
   * `get_augmented_files <Augmenter-get_augmented_files.html>`_
   * `get_annotated_image <Augmenter-get_annotated_image.html>`_

   .. note::
      The `torchvision.transforms` module is used for image transformations. For more information, refer to the `torchvision documentation <https://pytorch.org/vision/stable/transforms.html>`_.

   .. note::
      The `cv2` (OpenCV) library is used for image processing. For more information, refer to the `OpenCV documentation <https://docs.opencv.org/master/index.html>`_.

   .. note::
      The `torchvision.tv_tensors.BoundingBoxes` class is used for representing bounding boxes. For more information, refer to the `torchvision documentation <https://pytorch.org/vision/stable/_modules/torchvision/tv_torch.html#BoundingBoxes>`_.
