# vehicle_image_classification

### Énoncé :
Dans cet exercice, nous allons réaliser un modèle de classification
d'images à l'aide de la bibliothèque Keras. Le jeu de données à utiliser est
libre, mais il devra contenir au minimum deux classes. De plus, une
explication devra être fournie dans votre fichier Readme. En ce qui
concerne le nombre d'échantillons, je vous recommande d'avoir un peu
plus de 100 images par classe.

### Requirements
```bash
# From command line
pip install numpy pandas matplotlib scikit-learn keras tensorflow keras-tcn mega.py

# Or from notebook
!pip install numpy pandas matplotlib scikit-learn keras tensorflow keras-tcn mega.py
```

### Code :

<a target="_blank" href="https://colab.research.google.com/github/pthavarasa/vehicle_image_classification/blob/main/Vehicle_Image_classification.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### résultats
| Model | Accuracy | precision | recall | f1-score |
| :- | -: | -: | -: | -: |
| CNN | 70 | 71 | 71 | 71
| CNN with dropout | 64 | 68 | 64| 65
| CNN Multiple Convolutional Blocks | 64 | 68 | 64 | 66
| Convolutional Neural Network with Regularization | 42 | 45 | 39 | 40
| EfficientNet | 82 | 84 | 85 | 84

### Méthode de prédiction
Pour utiliser que la méthode de prédiction, suivre les étapes suivants :

1. Téléchargez et installez les packages et leurs dépendances. (bloc 2.1)
2. Importation des bibliothèques et modules nécessaires. (bloc 2.2)
3. Exécuter la cellule contient la login MEGA une fois que l'identifiant est remplie. (bloc 2.3)

Si vous n'ête pas conserné par les personnes qui ont eu l'identifiant partager, télecherger les models + tokenizer manuellement et importer sur colab.

  - CNN : https://mega.nz/file/EYNHUZ7A#qZvYARtKcb05LJhsQW1bfoDcK0oJhUbgU_NsVFG3RUQ
  - CNN with dropout : https://mega.nz/file/EYNHUZ7A#qZvYARtKcb05LJhsQW1bfoDcK0oJhUbgU_NsVFG3RUQ
  - CNN Multiple Convolutional Blocks :  https://mega.nz/file/EYNHUZ7A#qZvYARtKcb05LJhsQW1bfoDcK0oJhUbgU_NsVFG3RUQ
  - CNN with Regularization : https://mega.nz/file/8VtjXSyA#c7WOoBiuK0ml_TJhCX95aLvn--anlnS2NNpPyKxzDig
  - EfficientNet : https://mega.nz/file/0FkglCjb#l_MXYl2iBJR92s-NWIooi5o9r5va-4ioCrjC5Nvumt8

### Les techniques
- Data augmentation
  * `rotation_range=20` : fait pivoter les images de manière aléatoire dans une plage de 20 degrés.
  * `width_shift_range=0.2` : décale aléatoirement la largeur (horizontale) des images de 20 % de la largeur totale.
  * `height_shift_range=0.2` : décale aléatoirement la hauteur (verticale) des images de 20 % de la hauteur totale.
  * `shear_range=0.2` : applique de manière aléatoire des transformations de cisaillement aux images dans une plage de 20 degrés.
  * `zoom_range=0.2` : zoome aléatoirement sur les images jusqu'à 20 %.
  * `horizontal_flip=True` : Retourne aléatoirement les images horizontalement.
  De plus, `validation_split=0.2` est spécifié pour indiquer que 20 % des données seront réservées à la validation. Cela signifie que le générateur de données divisera automatiquement les données, avec 80 % utilisés pour la formation et 20 % pour la validation.
- Modèles
  - CNN
  - CNN with dropout
  - CNN Multiple Convolutional Blocks
  - Convolutional Neural Network with Regularization
  - EfficientNet
- Métrique
  - Accuracy
  - Precision
  - Recall
  - F1 score

### Source
- https://www.tensorflow.org/tutorials/images/cnn?hl=fr
- https://www.analyticsvidhya.com/blog/2020/10/create-image-classification-model-python-keras/
