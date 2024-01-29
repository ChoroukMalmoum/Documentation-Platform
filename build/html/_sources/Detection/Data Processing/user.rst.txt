Data Handling and Preparation
+++++++++++++++++++++++++++++

Data handling and preparation are crucial steps in the workflow of our Object Detection App. This process involves importing images, annotating them with bounding boxes, augmenting the data for diversity, and exporting the prepared data for further use. 
The prepared data can then be used to train the `model <./_model/user.html>` that will be selected later. Each of these tasks is designed to ensure the quality and suitability of the data for object detection tasks, providing a seamless workflow from data import to model training.

**Importation**
---------------

a. **Local Importation**
==============================
       The `FilesHandler <FilesHandler.html>`_ class Handles a collection of files, separating them by type and performing default handling.

       - **Remove empty Method:**
         `remove_empty <FilesHandler-remove_empty.html>`_ : Removes empty files from the list of files.

       - **Pair Method:**
         `pair <FilesHandler-pair.html>`_ : Pairs image and label files based on their names.
        
       - **Separate files by type Method:**
         `separate_files_by_type <FilesHandler-separate_files_by_type.html>`_ : Separates files into two lists based on their types: images and labels.
        
       - **Default handling Method:**
         `default_handling <FilesHandler-default_handling.html>`_ : Performs default handling of files:

           1. Removes empty files.
           2. Separates files by type (images and labels).
           3. Pairs images and labels based on names.

b. **External Importation**
==============================
   The `FileCsvHandler <FileCsvHandler.html>`_ class Handles CSV files containing image links and labels.

   - **Fetch Images Method:**
     `fetch_images <FileCsvHandler-fetch_images.html>`_ : Fetches images from the provided image links.

   - **Pair Method:**
     `pair <FileCsvHandler-pair.html>`_ : Pairs images with labels and handles empty labels.

   - **Remove Empty Method:**
     `remove_empty <FileCsvHandler-remove_empty.html>`_ : Removes pairs with empty images or labels.

   - **Default Handling Method:**
     `default_handling <FileCsvHandler-default_handling.html>`_ : Performs default handling of the CSV file:


    .. note:: 
      In this module, as well as in others, processed files are required to furnish their names. Consequently, an extended file-like class has been implemented to facilitate this handling.

      .. class:: NamedBytesIO(BytesIO)

      A subclass of BytesIO with an additional 'name' attribute.

      :param initial_bytes: Initial bytes for the BytesIO.
      :type initial_bytes: bytes, optional
      :param name: The name associated with the BytesIO object.
      :type name: str, optional

      :ivar name: The name associated with the BytesIO object

**Image Handling**
-------------------------

a. **Image Transformation**
==============================
   The `ImageTrans <ImageTrans.html>`_ class is designed for transforming and annotating images with bounding boxes.

   - **Get image boxes Method:**
     `get_image_boxes <ImageTrans-get_image_boxes.html>`_ : Extracts image and bounding box information from input data.

   - **Bounding box method:**
     `bounding_box <ImageTrans-bounding_box.html>`_ : Draws bounding boxes on the image.

   - **Show Method:**
     `show <ImageTrans-show.html>`_ : Displays the image with bounding boxes using OpenCV.

   - **Get annotated image Method:**
     `get_annotated_image <ImageTrans-get_annotated_image.html>`_ : Returns an annotated image with bounding boxes.

b. **Showing Images**
==============================
   The `ImageShow <ImageShow.html>`_ class is designed for displaying a grid of images.

   - **Show Method:**
     `show <ImageShow-show.html>`_ : Displays a grid of images using Matplotlib.
       .. note::
          The `Matplotlib` library is used for creating plots and displaying images. For more information, refer to the `Matplotlib documentation <https://matplotlib.org/>`_.

       .. note::
          The `PIL (Python Imaging Library)` is used for handling image data. For more information, refer to the `PIL Documentation <https://pillow.readthedocs.io/en/stable/>`_.

**Data Augmentation**
-------------------------
   The `Augmenter <Augmenter.html>`_ class is designed for data augmentation on images and bounding boxes.

   - **Augment Method:**
     `augment <Augmenter-augment.html>`_ : Applies specified augmentations to the image and bounding boxes.

   - **Get Augmented Files Method:**
     `get_augmented_files <Augmenter-get_augmented_files.html>`_ : Returns augmented image and label as NamedBytesIO objects.

   - **Get Annotated Image Method:**
     `get_annotated_image <Augmenter-get_annotated_image.html>`_ : Returns annotated image with bounding boxes.

**Data Exportation**
-------------------------
   The `Exporter <Exporter.html>`_ Class for exporting paired image and label data to a local directory.

   - **Augment Method:**
     `split_data <Exporter-split_data.html>`_ : Splits the paired data into training, validation, and test sets.

   - **Get Augmented Files Method:**
     `export_local <Exporter-export_local.html>`_ :  Exports the paired data to a local directory.

   - **Get Annotated Image Method:**
     `default_handling <Exporter-default_handling.html>`_ : Performs the default handling of data export.


