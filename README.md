# DSAP_SER
Information about the code: 
## Creating the data sets
file: DATA_PREPROCESSING.ipynb
1. Zeropad all files to same length
2. For every emotion copy corresponding files in two folders: /[emotion] and /not[emotion]
3. Create folder with balanced dataset out of step 2
4. Repeat all files to same length
5. see which files are in the zeropadded datasets and create the same datasets with repeated files
## Plots of validation loss and accuracy during training
file: Learning_Plots.ipynb
Unfortunately we made a coding mistake when saving training loss. So we cannot display that
## Training + Results
files: [technique]_[input]_[emotion]  
Few notes:
*  We did not clean code properly so there might be some artifacts like dropout layer (we considered it but then did not really use it)
*  Names of the folders where we save data does not make sense in some cases
*  Trainingsloss not obtained correctly
*  A few files seemed to be defect after preprocessing (as mentioned, we had problems with drive). Thats why this line is there: if not torch.isnan(input_save.unsqueeze(1)).any():

