TensorflowModels.download_model
+++++++++++++++++++++++++++++++

.. method:: TensorflowModels.download_model()

    Downloads the model from the specified URL.

    This method downloads a tar.gz file from the `model URL <tfmodels.html>`_, extracts it, 
    and saves it to the 'PRETRAINED_MODEL_PATH'. If the model already exists 
    at the 'PRETRAINED_MODEL_PATH', the download is skipped.

    :raises urllib.error.URLError: If there is an error during the model download.
    :raises tarfile.ReadError: If there is an error during the extraction of the model.
    :raises Exception: If an unexpected error occurs.