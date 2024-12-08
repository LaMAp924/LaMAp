# LaMAp
# Neural Network Training and Optimization (MLP) with Genetic Algorithms (GA)

This repository contains MATLAB files (tested with version 2024b) for **training Multilayer Perceptron (MLP) Neural Networks** and optimizing these networks using **Genetic Algorithms (GA)**, as described in Supplement 4 of the associated article. It is designed to allow the efficient and customizable creation, training, and optimization of MLPs.

To ensure proper functionality, all files must be in the **same folder**. The system has been tested on **Windows 10**, and the necessary input files for training and validation are included in the repository.

## Main Files

The repository contains two main MATLAB files:

**1️⃣ RNACreator.m**  
This file is responsible for creating and training the Multilayer Perceptron (MLP) Neural Networks. The user can define the number of input variables, the number of neurons per layer (with a maximum of 3 layers), the desired accuracy criterion, and the maximum number of iterations (defined by the "Generation" parameter). The training continues until the specified accuracy criterion is met or the iteration limit is reached. Once training is complete, the networks are sent to the optimization phase in the **AlgoritmoGenetico.m** file.

**2️⃣ AlgoritmoGenetico.m**  
This file performs the optimization of the trained networks using Genetic Algorithms (GA). The process includes operations such as selection, migration, crossover, and mutation. By default, **20% of the best-trained networks** are selected, **15% are migrated**, and a **mutation rate of 5%** is applied to introduce variations into the networks. The default loss function used is **cross-entropy**, but it can be manually modified by the user.

## Required Input Files

The following input files are required for proper functionality:

- **input_treinamento**: Contains the input data used to train the neural networks.
- **output_treinamento**: Contains the output data used for blind testing and model validation.

Both input files must be in the same folder as the main MATLAB files.

## Configurations

The repository allows customization of several parameters, which can be adjusted directly in the **RNACreator.m** and **AlgoritmoGenetico.m** files. The key configurations include:

- Number of input variables;
- Network structure (number of layers and neurons);
- Desired accuracy criterion;
- Maximum number of iterations (set by the "Generation" parameter);
- GA parameters such as selection, migration, and mutation rates;
- Loss function (cross-entropy by default, but can be modified).

## Execution Flow

1. **Training with RNACreator.m**: The user configures the number of input variables, network structure, accuracy criterion, and iteration limit. The system creates and trains the networks until the accuracy criterion is met or the iteration limit is reached.

2. **Optimization with AlgoritmoGenetico.m**: The trained networks are optimized using Genetic Algorithms. The process applies selection, migration, crossover, and mutation to generate more efficient networks. The percentages for selection (20%), migration (15%), and mutation (5%) can be adjusted directly in the code.

## Final Notes

This repository provides a complete solution for **training and optimizing Multilayer Perceptron (MLP) Neural Networks**. The system allows customization of various parameters, from network structure to optimization operations. With the appropriate adjustments, users can explore network configurations that maximize model performance. The code has been tested on **Windows 10**, ensuring stability and compatibility.

For questions or suggestions, feel free to explore the code and adjust the configurations to fit your project's needs.
