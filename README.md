# ECG_Heartbeat_Classification

Requirement : Keras, tensorflow, numpy 

# Heartbeat Classification : Detecting abnormal heartbeats and heart diseases from
ECGs

An ECG is a 1D signal that is the result of recording the electrical activity of
the heart using an electrode. It is one of the tool that cardiologists use to
diagnose heart anomalies and diseases.


### Dataset

<span class="figcaption_hack">Figure 2 : Example of preprocessed sample from the MIT-BIH dataset</span>

MIT-BIH Arrhythmia dataset :

* Number of Categories: 5
* Number of Samples: 109446
* Sampling Frequency: 125Hz
* Data Source: Physionet’s MIT-BIH Arrhythmia Dataset
* Classes: [’N’: 0, ‘S’: 1, ‘V’: 2, ‘F’: 3, ‘Q’: 4]

The PTB Diagnostic ECG Database

* Number of Samples: 14552
* Number of Categories: 2 ( Normal vs Abnomal)
* Sampling Frequency: 125Hz
* Data Source: Physionet’s PTB Diagnostic Database


### Model

Similar to [1] I use a neural network based on 1D convolutions but without the
residual blocks :

<span class="figcaption_hack">Figure 3 : Keras model</span>

Code :

### Results

MIT-BIH Arrhythmia dataset :

* Accuracy : **98.5**
* F1 score : **91.5**

The PTB Diagnostic ECG Database

* Accuracy : **98.3**
* F1 score : **98.8**

### Transferring representations


From Scratch :

* Accuracy : **98.3**
* F1 score :** 98.8**

Freezing the Convolution Layer and Training the Fully connected ones :

* Accuracy : **95.6**
* F1 score : **96.9**

Training all layers :

* Accuracy : **99.2**
* F1 score : **99.4**
