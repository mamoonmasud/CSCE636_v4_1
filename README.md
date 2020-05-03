# CSCE636_v4_1
GitHub repo containing the codes for the final submission of the Action Recognition Project (Kinetics I3D Architecture)  
These files are part of the course project for the Course CSCE 636 : Deep Learning by Dr. Anxiao Jiang
Final Submission: 

For this submission, two models are being submitted. One is a fine tuned version of the previous submission, and the rest of the model details are same. The other model being submitted is based on Quo Vadis [6] 
The major improvements for this step were the use of an architecture suggested by Dr. Jiang, using transfer learning, fine tune a model trained on Kinetics and ImageNet Datasets. 

Architecture

The architecture is baed on Two-Stream Inflated 3D Conv Nets. In order to incorporate temporal information, the model starts with a 2D architecture, and inflating all the filters and pooling kernels, endowing them with additional dimensions (temporal). So, filters then become 3 dimensional from 2 dimensional. Since CNN only performs pure feedforward computations, this architecture also proposed generating optical flow, and using it as inputs to train another I3D network, however optical flow is not being used for our project. 

The model architecture of the Inception-v1 Inflated 3D ConvNet, which were used with trained weights on ImageNet and Kinetics Dataset is given in the GitHub repo (https://github.com/mamoonmasud/CSCE636_v4_1)
The trained model is loaded, but without the classification layers. A CNN, LSTM and Dense layers are added once the features are extracted by the trained model for classification purpose. 
