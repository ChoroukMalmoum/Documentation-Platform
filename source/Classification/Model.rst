Model Selection
+++++++++++++++++++

Once data is imported, the next step involves selecting a model for image classification. The application provides three distinct options to accommodate various user preferences and requirements:

1. **Build Your Own Model:**
------------------------
For users who prefer a customized approach to model creation, the "Build Your Own Model" option provides a code-free interface to design and configure a unique neural network tailored to their specific image classification task.

Step-by-Step Configuration:
      a. **Input Layer:**
        -Set the input height and width (e.g., 225 x 225) to match the dimensions of your input images.
      
      b. **Convolutional Layer:**
        -Determine the number of filters (e.g., 32) for feature extraction.
        -Specify the filter height and width (e.g., 3 x 3) to define the convolutional kernel size.
        
      c. **MaxPooling Layer:**
        -Set the pool height and width (e.g., 2 x 2) for down-sampling and retaining essential features.
            
      d. **Flatten Layer:**
        -This layer prepares the data for input into the dense layers. No adjustable parameters are required.
     
      e. **Dense Layer:**
        -Decide on the number of units (e.g., 64) to configure the densely connected layer.
      
      f. **Output Layer:**
        -Tailor the output layer based on your specific data and classification task. The configuration will depend on the number of classes in your dataset.
      
      g. **Additional Options:**
        -Users have the flexibility to add or drop layers based on their preferences, allowing for fine-tuning and experimentation.

- Refer to the `tensorflow documentation <https://www.tensorflow.org/tutorials/images/classification>`_ for more details on the layers used. 
  

2. **Upload Your Model:**
------------------------
If you already have a trained model, choose this option.
    - Upload an h5 file 
    - Upload a zipped file containing the h5 model file.

Users can seamlessly integrate their pre-existing models into the application, ensuring continuity in their image classification projects.


3. **Choose a Pretrained Model:**
------------------------

The "Choose Pretrained Model" option offers users the convenience of leveraging established and well-performing models for image classification. This approach is particularly beneficial for users seeking a quick start or for those who prefer not to build a model from scratch. The application provides a selection of four popular pretrained models:

      a.**MobileNetV2:**

        -A lightweight and efficient model designed for mobile and edge devices.
        -Ideal for scenarios with limited computational resources without compromising accuracy.

      b.**ResNet50:**

        -A deep residual network with 50 layers, known for its excellent performance in image recognition tasks.
        -Well-suited for diverse datasets and complex image classification challenges.

      c.**DenseNet121:**

        -A densely connected convolutional network with 121 layers.
        -Facilitates feature reuse and enables efficient information flow through the network.

      d.**VGG16:**

        -A classic deep learning architecture with 16 layers.
        -Recognized for its simplicity and effectiveness in capturing hierarchical features.

The "Choose Pretrained Model" option streamlines the model selection process, allowing users to benefit from the knowledge embedded in well-established architectures without the need for extensive training or customization.


Model Training
+++++++++++++++++++

After selecting the model, the next crucial step is training it on your data to enhance its predictive capabilities.


1. **Choose Layers for Training:**
------------------------

      -Customize the training process by selecting specific layers for training.
      -Opt to train the entire model or focus on specific layers for fine-tuning.

This flexibility allows users to adapt the training strategy based on their dataset and objectives.


2. **Set Hyperparameters:**
------------------------

Fine-tune the training process by configuring these hyperparameters:

      -Learning Rate: Determines the step size during the optimization process.
      -Batch Size: Specifies the number of data points used in each iteration.
      -Number of Epochs: Defines the number of times the model iterates over the entire dataset.

Adjusting these hyperparameters enables users to optimize the model's learning process for better performance.

3. **Monitoring the Training:**
------------------------

      -As the model iterates through epochs, real-time updates on accuracy and loss are streamed through Socket.IO.
      -Users can observe the dynamic behavior of these metrics, gaining insights into the model's convergence and       
       performance improvements.

During the training process, the application provides a dynamic and real-time monitoring display, enhancing the user's ability to track the model's progression effectively. Leveraging Socket.IO, the application delivers live updates on crucial metrics, including accuracy and loss. 

- Refer to the `Socketio documentation <https://python-socketio.readthedocs.io/en/stable/>`_ for more details on the Socketio implementation.  
