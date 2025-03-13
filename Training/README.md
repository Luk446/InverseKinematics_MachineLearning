Folder containing the main notebook that is used for the network training 


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
