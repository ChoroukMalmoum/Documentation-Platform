TensorflowModels.eval
++++++++++++++++++++++

.. method:: TensorflowModels.evaluate_model()

    Evaluates the model.

    This method runs a script that evaluates the model using the 'pipeline.config' 
    and the checkpoints in the 'CHECKPOINT_PATH'. The evaluation is performed until 
    a timeout of 120 seconds is reached.

    :return: The command used for evaluation, if the operating system is POSIX.
    :rtype: str
    :raises subprocess.CalledProcessError: If there is an error during the execution of the evaluation script.