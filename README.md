# Chimera
`Chimera` is a Python package for distributed machine learning (DML).

It supports the following types of DML:

- Data Parallelism: data distributed between the workers. Each worker has a copy of the model. This case includes Distributed SGD (Stochastic Gradient Descent) for generic neural network architectures.
- Model Parallelism: model distributed between the workers. Each worker has a copy of the dataset. This case includes Distributed Ensemble Learning with generic weak learners from the `scikit-learn` package.

The implementation is Docker-based, that is, it uses docker containers to act as workers. To run the created distributed system, it will be given an standardized interface which will leverage a REST API server, on whose backend workers will run.

The communication between workers is made by message passing via the TCP protocol.
