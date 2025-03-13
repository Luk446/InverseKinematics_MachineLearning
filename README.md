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

![image](https://github.com/user-attachments/assets/13d562b0-f32f-4285-a70f-c745e9ece034)

1.	Model Loading 
-	Eight pre-trained models are loaded from pickle files.
2.	Evaluation Function 
-	An evaluation function (eval) is defined to evaluate a model on the test data.
-	The function calculates three metrics: Mean Absolute Percentage Error (MAPE), Mean Squared Error (MSE), and Mean Absolute Error (MAE).
3.	Model Display/Eval 
-	All eight models are evaluated using the defined evaluation function.
-	The results (MAPE, MSE, MAE) for each model are printed in a tabular format.
4.	Model Inspection 
-	The architecture, optimizer configuration, and summary of a selected model (Model 2) are printed.
-	Summaries of all models are printed, showing the layer configurations and parameter counts.

Overall, the notebook automates the process of evaluating multiple trained models, compares the performance metrics, and inspects the architectures

## Script 3 - Export Eval

Similar to the second script although now there is additional functionality to export the target and output of the network, and only one model is evaluated

