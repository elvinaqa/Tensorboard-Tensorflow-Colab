# Tensorboard-Tensorflow-Colab
Tensorboard implementation in Google Colab (Tensorflow)


Start by installing TF 2.0 and loading the TensorBoard notebook extension:

For Jupyter users: If you’ve installed Jupyter and TensorBoard into the same virtualenv, then you should be good to go. If you’re using a more complicated setup, like a global Jupyter installation and kernels for different Conda/virtualenv environments, then you must ensure that the tensorboard binary is on your PATH inside the Jupyter notebook context. One way to do this is to modify the kernel_spec to prepend the environment’s bin directory to PATH, as described here.

![Screenshot (176)](https://user-images.githubusercontent.com/57037068/83444629-b5aa3a00-a45c-11ea-8960-ac46c338c1f8.png)

In case you are running a Docker image of Jupyter Notebook server using TensorFlow's nightly, it is necessary to expose not only the notebook's port, but the TensorBoard's port.

Thus, run the container with the following command:

docker run -it -p 8888:8888 -p 6006:6006 \
tensorflow/tensorflow:nightly-py3-jupyter 
where the -p 6006 is the default port of TensorBoard. This will allocate a port for you to run one TensorBoard instance. To have concurrent instances, it is necessary to allocate more ports.
# Load the TensorBoard notebook extension
%load_ext tensorboard




