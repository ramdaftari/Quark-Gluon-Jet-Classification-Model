# Quark-Gluon-Jet-Classification-Model

Some Important Notes
- Every entry int the dataset had a maximum multiplicity of particles - this maximum multipllicity differed which caused me problems while flattening. Hence, I split up each particle individually into an entry
  and each event was alloted a related ID
- I first tried a random forest classification model which had a fairly low accuracy
- Then moved to a Gradient Boosting LightGBM model
- In the LightGBM model, during initial training, data analysis showed that the dataset was significantly unbalanced
  Hence, too get a comprehensive view of the picture, I concatented three different datasets and then further balanced the dataset due to SMOTe
- Due to lack of computational power, I had to cut down the dataset to 1/3rd random entries of the above
- Then, I trained a random LightGBM model on it
- Tried Hyperparameter tuning using Bayesian optimisation, which was a learning opportunity albeit not drastically improving accuracy
