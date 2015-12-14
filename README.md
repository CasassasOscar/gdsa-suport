## Suport i entregues setmanals

### Eina d'issues
Plantegeu els vostres dubtes obrint un nou issue en aquest repositori.

### Instruccions per les entregues setmanals

Busqueu l'issue de l'entrega corresponent (El títol dels issues d'entrega és la data límit).

Responeu l'issue amb un missatge amb el nom del vostre equip i l'enllaç públic a la presentació a Google Drive.

## Code Instructions

### Setup

- Edit the file `src/params.py` so that `params['root']` points to the directory where you have the dataset `TerrassaBuildings900` and where you would like to store all the intermediate files. You can also modify some of the parameters there (such as the codebook size, the keypoint detector, etc.)
- Run `src/params.py`. Notice that this will create directories as well, so make sure you did the previous step !
- Run `src/build_database.py` to generate text files with image IDs for both the training and validation sets. 

### Feature extraction

- Run `src/get_features.py`. This will first train a codebook, and then build BoW vectors for the training and validation/test images.

### S5: Ranking Instructions

- Run `src/rank.py` to compute distances from validation images to train images and generate the rankings.
- Run `src/eval_rankings.py` to obtain the mean Average Precision of your rankings.
- For a step by step tutorial and a better analysis of the results, check `notebooks/gdsa_s5.ipynb`

### S6: Classification Instructions

- Run `src/classify.py`. This will train a classifier and use it to predict classes for validation images.
- Run `src/eval_classification.py` to get evaluation metrics of your classifier predictions.
- Check `notebooks/gdsa_s6.ipynb` to see a tested example.

## Results

You can check the leaderboard in the [repository website](http://gdsa-upc.github.io/gdsa-suport/).
