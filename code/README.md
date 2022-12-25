## Dataset
You can find the augmented dataset [here](https://mega.nz/file/6FRRhajS#BQfDQwlE5bf9Vm-1G2JU2SPkHU-dWYDS4cTryPUSZjQ)

Please download the augmented dataset in ./ folder and unzip it.
If you want, you can use the original dataset and generate the augmented dataset using
the 'Data_analysis.ipynb' notebook. Keep in mind the generation may take up to 50 minutes.


## Data analysis notebook
this notebook contains:
- outliers analysis 
- data scaling with robust scaling
- sliding window generation

## best_model notebook
Generates the last model submitted to codalab. Our idea was to direct each timeseries to a specific net, responsible to extract relevant features for the given timeseries, concatenate the results and finally sending them to the classifier through a GlobalAveragePooling1D and 2 fully connected layers.

<img src="https://user-images.githubusercontent.com/62434812/209477922-e0819bdf-fd4a-4dfe-be32-ac2196ebc24e.png" width="400" height="800" />

After reaching promising results, we discovered we accidentally sent the whole input to all the heads, so this model doesn't seems to have much sense, still, this is the best model we were able to produce, indeed, this version outperforms the correct one.
