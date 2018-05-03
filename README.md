# Collaborative Filtering Recommendation Engine #
A Recommender System based on the Collaborative Filtering Techinique

## Running Instructions ##
All of these commands should be issued from the main directory of the repository.
### Setup ###
```
pip install -r requirements.txt
```

### Training ###
```
python Code/runner.py --mode train --algorithm insert_algorithm_here --model-file algorithm's_name.model --data Data/ratings.csv
```

### Predicting ###
```
python Code/runner.py --mode test --algorithm insert_algorithm_here --model-file algorithm's_name.model --num-neighbors default_is_five --data Data/ratings.csv --predictions-file insert_algorithm_here.predictions
```

### Evaluation ###
```
python Code/eval.py Data/ratings.csv algorithm's_name.predictions
```

### Running Testing Suite ###
```
python test.py
```

### Algorithm Names (for command line arguments) ###
* pearson
* spearman
* mean_squared
* cosine
