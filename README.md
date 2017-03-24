# Using the TUSCAN predictor

On-target component of the [GT-Scan](http://gt-scan.net) suite.

**Clone the Git repository**
You need to have [Git-LFS](https://git-lfs.github.com) installed on your computer to handle one file that is larger than the 100MB file size limit of github.

**Building a model**  
To build classifier, run
```
python ModelBuilder.py -c ClassificationMatrix.txt ClassificationFeatures.txt
```

To build regressor, run
```
python ModelBuilder.py -r RegressionMatrix.txt RegressionFeatures.txt
```

This builds models and stores them in joblib binaries

**Predicting using a model**  
Run ModelPredictor with FeatureMatrix.py, your joblib files and the relevant list of features in the same directory

Usage:
```
python ModelPredictor.py -i Infile -o Outfile -m Regression/Classification -t InfileType (fasta/bed/txt) -g genome (if supplying bed file)
```

Use -h for Help
