The Jupyter Notebook “Notebook_Fuzzy_Logic” is a collection of Python3 scripts aimed at developing a classification algorithm able to separate biological targets from meteorological targets (precipitation) and clutter.

When running the notebook, be sure have in your folder the file “odimh5_file.py”, which contains functions to process ‘h5’ files. 

The rationale of this work is described in “Fuzzy_Logic.pptx”, and it is also illustrated step by step in the notebook.

Basically, polarimetric and non-polarimetric radar variables, plus variables derived from them, are used to create the classification algorithm based on fuzzy logic. Here is a summary:
- There are three classes to identify: biological targets, precipitation, and clutter.
- There are also several variables (polarimetric and non) to be used.
- For each variable, a Membership Function for each class is extracted from the data.
- The overlapping of the membership functions belonging to the three classes defines the importance of the variable in the classification algorithm, or the variable weight.
- Once all the weights are calculated, the membership functions can be combined to create the Aggregation Value for each of the three classes.
- Once the algorithm is trained, the aggregation value can be calculated for each radar pixel.
- The pixel is assigned the class with the highest aggregation value.

All the volume radar data used in this notebook have been uploaded to the Data folder. Inside this folder there are three additional folders (bio, precipitation, clutter) that include a few data files for each class that have been used to train the algorithm. 

The variables extracted from these files are collected in ‘csv’ files uploaded to the same Data folder: “bio_data.csv”, “precipitation_data.csv”, “clutter_data.csv”.
