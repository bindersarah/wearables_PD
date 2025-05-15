# Wearables in PD Machine Learning Project 
End of term project for CISC5800 Machine Learning at Fordham University.

## Aim 1
Predict movement state (sit-to-stand, sitting, turn, turn-to-sit, walk) from the Timed-Up-and-Go (TUG) task

### Models
Executes 2 models to predict movement state across a cohort of control and diagnosed PD participants via grouped-k-fold cross validation:
  1. Lasso Logistic Regression
  2. SVM with a gaussian kernel, with PCA performing dimensionality reduction

### Key Files
  1. Get_Synapse_Data (via programmatic download)
  2. Wearables_Aim1 (preprocessing and model deployment)

## Aim 2
Predict cohort (control or Parkinson's Disease)

### Model
Builds CNN from TUG and walking tasks. 
Model success comes from convolutional layers for feature extractin: employing smaller kernels to detect fine-grained motion like PD tremors, and larger kernels to detect gait impairment and bradykinesia.

### Key Files
  1. Get_Synapse_Data
  2. Preprocess_aim2 (performs windowing, splits data with groupshufflesplit to extract a holdout set for testing)
  3. MLW_train_cnn (builds and trains CNN, evaluation done on holdout data, using model with best val_accuracy)

## Data Source
https://www.synapse.org/Synapse:syn52540892/wiki/623751
