# InverseKinematics_MachineLearning
Level 4 thesis project 

*Due to sensitivity of data the project folder cannot be public*

Coding is comprised of two scripts, compiled in Visual Studio Code Jupyter Notebooks.

## Script 1 - MLPR Training

The first notebook contains the training algorithm for the MLPR, designed to train a machine learning model to solve an inverse kinematics problem using PyTorch and Ray Tune for hyperparameter optimization.

![image](https://github.com/user-attachments/assets/a61683d4-3792-4d98-8099-ae1943472496)

1.	Library Imports 
-	Essential libraries for machine learning (PyTorch), hyperparameter tuning (Ray Tune), data manipulation (Pandas, NumPy), and other utilities are imported.
2.	Data Handling 
-	Data is imported from a CSV file (All_data.csv)
-	The data is split into input features (I for positional data) and target values (C for actuation data).
-	The data is further split into training, validation, and test sets.
-	The input features and target values are normalized and converted into PyTorch tensors.
3.	Model Definition 
-	A multi-layer perceptron (MLP) regressor class (MLPRegressor) is defined with configurable hidden layers, activation functions, and dropout layers.
4.	Training Function 
-	The train function is defined to train the MLPRegressor model.
-	It includes model initialization, device allocation, optimizer selection, data loaders creation, checkpointing, and training and evaluation loops.
-	The function also reports training progress and metrics to Ray Tune.
5.	Hyperparameter Tuning 
-	The main function sets up Ray Tune for hyperparameter optimization.
-	It defines the hyperparameter search space and uses an ASHA Scheduler for early stopping of underperforming trials.
-	The function allocates resources dynamically based on availability and runs the hyperparameter search.
-	The best trial is identified, and the best trained model is saved.
6.	Execution 
-	The notebook includes a block to initialize Ray and call the main function to start the hyperparameter tuning and training process.

Overall, the notebook automates the process of training a neural network model, optimises its hyperparameters, and saves the best-performing model for solving an inverse kinematics problem.

##Script 2 - Evaluation

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

