# S24-AISec Midterm Tutorial
This folder contains 2 tutorial notebooks and sample code for the deployment process of the MalConv assignment (AKA The Original Midterm).

In these tutorials, it is assumed that you have already completed the training of your MalConv model, and have saved the model as either a checkpoint file (.pt) or Paths file (.pth). 

To begin the tutorial, first go to your AWS SageMaker Dashboard -> Notebooks and create a new notebook instance. Once instantiated, open the Jupyter server (not Jupyter Lab), and upload the following files:


1.   Your model checkpoint/paths file, e.g., model.pt

2.   Create a new folder named ``code``, and upload ``inference.py`` there.

3.   Upload MalConv-Deploy.ipynb in the home directory (not in /code).

4.   Open MalConv-Deploy.ipynb, and when prompted, select the ``conda_pytorch_p310`` kernel.

Once your model endpoint is deployed, then run the ``S24-AISec-Client.ipynb`` notebook either on Google Colab or your own device. 

Also, please be advised:


*   This sample implementation is not at all optimal, and can be improved in many ways.
*   This sample implementation is for a particular implementation of the MalConv architecture and data preprocessing. There is a good chance that you would need to modify at least the model definitions of inference.py for it to work with your own model.
*   Last but not least, please note that the deployment process is slightly different for non-Pytorch models. For instance, for SKLearn models, see [this example notebook](https://github.com/aws/amazon-sagemaker-examples/blob/main/sagemaker-python-sdk/scikit_learn_randomforest/Sklearn_on_SageMaker_end2end.ipynb).
