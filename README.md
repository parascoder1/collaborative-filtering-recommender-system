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

Upon running the test suite, a list of all the algorithms, their execution with different number of neighbours, their corresponding mean absolute erros and time taken for predictions (in seconds) is dislpayed.

### Algorithm Names (for command line arguments) ###
* pearson
* spearman
* mean_squared
* cosine

### Example ###
```
$ pip install -r requirements.txt
$ python Code/runner.py --mode train --algorithm spearman --model-file spearman.model --data Data/ratings.csv
$ python Code/runner.py --mode test --algorithm spearman --model-file spearman.model --num-neighbors 3 --data Data/ratings.csv --predictions-file spearman.predictions
$ python Code/eval.py Data/ratings.csv spearman.predictions
```



