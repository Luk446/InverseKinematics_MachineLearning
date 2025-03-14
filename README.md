# Level 4 thesis project mapping IK of soft medical robotics


*Due to sensitivity of data the project folder cannot be public*

Page contains three folders:

## Training
Notebook containing the training algorithm for the MLPR, designed to train a machine learning model to solve an inverse kinematics problem using PyTorch and Ray Tune for hyperparameter optimization.
- Overall, the notebook automates the process of training a neural network model, optimises its hyperparameters, and saves the best-performing model for solving an inverse kinematics problem.

## Evaluation
The ModelEval2 script will output a saved model in the format “PR_NR_T(trial number).pickle”. To evaluate each of these and display the mean average percentage error, a second script was created to test them all
- Overall, the notebook automates the process of evaluating multiple trained models, compares the performance metrics, and inspects the architecture
Now the highest performing model can be easily identified, ModelExportFullData is then written.
- Similar to above but now there is additional functionality to export the input output pairs of the network, and only one model is evaluated.

## Benchmarking 
Additional testing done with a benchmarking database to verify the functionality of the training optimisation system
