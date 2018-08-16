#### Avalinguo-Dataset-Speaker-Fluency-Level-Classification-Paper-Replication Data

---

**Abstract**

> Level assessment for foreign language students is necessary for putting them in the right learning group, but it is also a very
time-consuming task, so we propose to automate the evaluation of speaker fluency level by implementing machine learning
techniques. This work presents an audio processing system capable of classifying the level of fluency of non-native English
speakers using five different machine learning models. As a first step, we have built our own dataset, which consists of labeled
audio conversations in English between people ranging in different fluency domains/classes (low, intermediate, high). We
segment the audio conversations into 5s non-overlapped audio segments and thereafter perform feature extraction on them.
After this, we have tunned the appropriate number of Mel cepstral coefficients to be extracted extracted from the audios by
evaluating accuracy performance. Thereafter, we have added the zero-crossing rate, root mean square energy and spectral flux
features, proving that this improves model performance overall. Out of a total of 1424 audio segments, with 70% training data
and 30% test data, our trained models have achieved a classification accuracy as high as 94.39% (support vector machine), the
rest of our models have passed the 89% classification accuracy.

**Report:**

* Author Report Version: [Speaker Fluency Level Classification Using Machine Learning Techniques](https://github.com/agrija9/Avalinguo-Dataset-Speaker-Fluency-Level-Classification-Paper-/blob/master/Report/Report%20Final%20Draft.pdf).


**Additional material**

* Poster Slide (90x120 cm²)
Speaker Fluency Level Classification Using Machine Learning Techniques - Poster
![](https://github.com/agrija9/Avalinguo-Dataset-Speaker-Fluency-Level-Classification-Paper-/blob/master/Poster/Figures/RIIAA%20Poster%202018.gif)


**Related Work**

I have placed all the data related to this work in another repository. In order to experiment with the code of this repo, it is necessary to first download the data from that repository.
* [Avalinguo Audio Dataset for Speaker Fluency Classification ](https://github.com/agrija9/Avalinguo-Audio-Set)

**Dependencies**

* Anaconda 2 with Python 2.7. (Python 3.6 not tested yet)
* Librosa (audio visualization and feature extraction)
* Sci-kit learn
* Keras (Theano backend)
* Numpy, Matplotlib
* Pandas (data visualization)

**Jupyter Notebook**

A Jupyter Notebook (Python 2.7 Kernel) is added to illustrate the workflow. 

The scripts for feature extraction and classification are contained in the 
```Avalinguo Audioset Experiment.ipynb``` file and are all loaded in the notebook sequentally.

They can also be found as separate files in the ```Individual Scripts``` folder.

Once the audio files from the Avalinguo Audio Dataset have been donwloaded and are placed in the same folder of the Jupyter Notebook, running the Feature Extraction cell creates a numpy array corresponding to the computed features (```feature.npy```) and one for labels (```label.npy```). These files will be saved in the current directory.

Thereafter, one can proceed to train the models with these two files.

**Audio features extracted**
- MFCC
- ZCR
- Spectral Flux
- Root Mean Square Energy

**Classifiers implemented**
- Support Vector Machine (SVM)
- Random Forest (RF)
- Convolutional Neural Network (CNN)
- Multilayer Perceptron (MLP)
- Recurrent Neural Network (RNN)

**Accuracies obtained**
**Note**: out of 1424 audio clips from the Avalinguo Audioset, with 30% test data, the reached accuracies are the following:
- SVM: 94.39%
- RF: 93.45%
- MLP: 92.52%
- CNN: 92.75% 
- RNN: 89.01%

More details on the training hyper-parameters and accuracies achieved can be found in the ```Code/Experimental Results``` folder, as well as in the attached Report/Report Final Draft.pdf``` file.

