# OD-SGD -- OD-SGD: One-step Delay Stochastic Gradient Descent for Distributed Training
The implementation of OD-SGD is based on the popular deep learning framework [MXNet](https://github.com/apache/incubator-mxnet), and I just modify some source code files to adjust the execution orders of the operations. Therefore, the file list is almost the same with [MXNet](https://github.com/apache/incubator-mxnet). OD-SGD is proposed to imporve the distributed deep learning training performance via increasing the overlap ratio of computation and communication process.

# Features
* OD-SGD can be applied to both parameter-server based framework (MXNet, TensorFlow) and end-to-end frameworks (PyTorch, Caffe).
* For parameter-server based platforms, the global update in the server node makes use of Syhchronous SGD algorithm, while the local update in local workers can adopt differnt algoritms, while the compensation algorithm like DC-ASGD will be a better choice to ensure goode convergence accuracy.
* When training with OD-SGD, you need to speicify the local optimizer, local learning rate, steps to change the local learning rate through "--local-optimizer", "--locla-lr" and "--local-lr-steps".

# Ask Questions
Please send emails to xuyemaovip@nudt.edu.cn for more details.
