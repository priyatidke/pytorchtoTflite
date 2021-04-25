# pytorchtoTflite

Task 1: 

Convert the Pytorch model from this Repo | Google Drive to TensorFlow Lite model

Steps to convert the model:



1) PyTorch Model to ONNX Model

ONNX: Open Neural Network Exchange (ONNX) is an open format built to represent machine learning models. The best thing about ONNX is interoperability.

  a. Define SuperResolutionNet Model.
  
  b. Initialize the model with the pretrained weights.
  
  c. The Pytorch exporter can trace the model and save it to an ONNX file.

 2) ONNX Model to TensorFlow Model
 
       a. Load the ONNX file and import it to Tensorflow
       
       b. Exporting to TensorFlow graphs
 
3) TensorFlow Model to TFLite Model

       a. Load TensorFlow model from saved_model
       
       b. Create Concrete Function
       
       c. Load the concrete function into the TFLiteConverter
       
       d. Convert and Store the Model

Challenges:

i. Versions issue

ii. How to Define The Base Model

iii. Missing keys & unexpected keys in state_dict when loading self trained model

iv. Load tensorflow model for conversion

v. Select way to convert a TensorFlow model into TensorFlow Lite model

vi. Issues regarding Flex Ops

Resolved:

i. Installing supported Versions

ii. Select to define SuperResolutionNet Model

iii. Set strict=False for Missing keys & unexpected keys in state_dict when loading self trained model

iv. Used tf.saved_model.load() method to load tensorflow model

v. Used concrete function




