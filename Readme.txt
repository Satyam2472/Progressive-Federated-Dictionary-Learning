ReadMe File - Progressive Federated Dictionary Learning
________________




1. Python file - .ipynb
   1. Code is written in Python using Google Colab and cells could be directly run connecting Colab to its GPU.


2. We have three main parts in our code.
   1. Federated Learning
   2. Federated Dictionary Learning
   3. Progressive Federated Dictionary Learning


3. Important functions
   1. ‘Net’ Class - The neural network architecture utilized for federated learning on the CIFAR-10 dataset is described in this class.
   2. ‘FederatedDataset’ Class - To prepare and arrange the CIFAR-10 dataset for federated learning, a special dataset class was created.
   3. ‘create_curriculum_federated_datasets’ function - creates federated datasets using curriculum learning to ensure a varied class distribution across clients.
   4. ‘federated_train’ function - trains a model with the given learning rate, and number of epochs on a federated dataset.
   5. ‘learn_local_dictionary’ function - uses mini-batch dictionary learning to learn a local dictionary from the client's data.
   6. ‘federated_dictionary_learning’ function - uses client input to train local models for federated dictionary learning, then aggregates local dictionaries to produce a global dictionary.


4. Main Section
   1. The CIFAR-10 dataset is loaded.
   2. Federated datasets are created via curricular learning.
   3. Sets the neural network model's initial state.
   4. The model is trained using federated datasets.
   5. Federated dictionary learning is carried out.
   6. Plots the accuracy and loss curves for training.