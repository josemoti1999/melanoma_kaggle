## Silver Medal winning solution for SIIM-ISIC Melanoma Classification Challenge 2020

<ul>
  <li>Training a single model.  
    See notebook <a href='https://github.com/josemoti1999/melanoma_kaggle/blob/master/Triple_Stratified_KFold_with_TFRecords_Colab.ipynb'>here</a>
    <ul>
  <li>Different variants of efficient net backbones pretrained on imagenet was finetuned. Training was done with the help of Colab TPUs. 
  </li>
  <li>Datasets are loaded from the Google Cloud Storage Buckets with the help of address to the dataset. 
  </li>
  <li>Stratified KFold Cross Validation was used in order to see th performance of the datasets.
  </li>
  <li>Augmentations used - colour constancy, rotae/shear/soom, random masks
  </li>
  <li>Different combinations of datasets were used for better variation/ generalization.
  </li>
    </ul>
  </li>
  <li>Some hyperparameter searches done.
    <ul>
      <li>Dataset - ISIC2020, ISIC2020+ISIC2019</li>
      <li>Efnet variants - B0 to B7</li>
      <li>Optimizers - Nadam, Adam, SGD</li>
      <li>Loss - BinaryCrossEntropyLoss with/without label smoothing, Focal loss, Sigmoid focal loss</li>
      <li>5Fold/ 15 Fold Cross Validation</li>
      <li>Epochs - 10 to 30</li>
      <li>Retrain - with/without pseudo labels</li>
    </ul>
  </li>
  <li>Ensembling the base models.
    <ul>
      <li>Light Gradient Boosting with Bayesian optimization. 
        See notebook <a href='https://github.com/josemoti1999/melanoma_kaggle/blob/master/Triple_Stratified_KFold_with_TFRecords_Colab.ipynb'>here</a></li>
  
