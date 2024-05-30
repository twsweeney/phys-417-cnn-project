This repo is a collection of the notebooks used to complete the physics 417 neural networks course 

The aim of this project was to take a dataset of gravitational wave data and classify it into 4 categories: 
1. Binary Black Hole Merger (BBH)
2. Core Collapse Supernova (CCSN)
3. Glitch
4. Background 

To recreate the results in our poster the following steps should be taken.

1. Run the notebook titled "image_generation.ipynb" to create the spectrogram image dataset that will be fed into each classifier
2. Run the notebook titled "GW_Parent_Classifier.ipynb" to train a classifier to sort images into Signals and non signals. 
3. Run both of the other Classifier notebooks to train each child network. "glitch_bg_classifier.ipynb" is trained to classify glitch and background examples, while "signal_classifier.ipynb" is trained to classify BBH vs CCSN
4. Finally, run the "Model_Evaluation.ipynb" notebook to apply the test dataset on each of the three networks that were just trained. 

One will need to obtain the raw data file "GW2_Andy.h5" to do this analysis. 

One may wonder why each model is contained in a separate  notebook file and not within one large script or notebook. This choice was made due to the development of this project being done in google colab. Due to memory limitations and issues with clearing GPU memory, it was necessary  that each model be trained in a different  notebook. 

The code contained will need to have the specific file paths updated, but otherwise should run "as is". 