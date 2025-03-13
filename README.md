# InverseKinematics_MachineLearning
Level 4 thesis project 

*Due to sensitivity of data the project folder cannot be public*

Coding is comprised of three scripts, compiled in Visual Studio Code Jupyter Notebooks.

## Script 1 - MLPR Training

The first notebook contains the training algorithm for the MLPR, designed to train a machine learning model to solve an inverse kinematics problem using PyTorch and Ray Tune for hyperparameter optimization.

Overall, the notebook automates the process of training a neural network model, optimises its hyperparameters, and saves the best-performing model for solving an inverse kinematics problem.

## Script 2 - Evaluation

The first script will output a saved model in the format “PR_NR_T(trial number).pickle”
To evaluate each of these and display the mean average percentage error, a second script was created to test them all



Overall, the notebook automates the process of evaluating multiple trained models, compares the performance metrics, and inspects the architectures

## Script 3 - Export Eval

Similar to the second script although now there is additional functionality to export the target and output of the network, and only one model is evaluated

