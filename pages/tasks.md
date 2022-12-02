---
title: Program
background: /assets/theme/images/bckg.png
permalink: /program/
---

### **<span style="color:#2B547E">Invited talks</span>**
\
- Samaneh Nasiri – Harvard University, Boston, United States of America: 
    Generalizability of machine learning models for electrophysiology
- Michel JAM van Putten – University of Twente, Enschede, The Netherlands
    Deep Learning for detection of epileptiform discharges in human EEG recordings
- Alexandre Gramfort – Inria, Paris, France / Hubert Banville – InteraXon, Toronto, Canada: 
    Self-supervised machine learning for wearable EEG monitoring

&nbsp;  

### **<span style="color:#2B547E">Paper presentations</span>**
\
![alt text]({{ '/assets/theme/images/task2.png' | relative_url }}){: .rounded .float-end}
Data is the main ingredient for developing automated classifiers. Most researchers have focused on developing state-of -the-art AI architectures in order to achieve better classification performance in many diverse tasks. Recently, the concept of ‘data-centric AI’ has risen as a promising option for achieving higher and better performances in hard classification problems.

Usually, training a model with high volumes of data tends to aid its robustness and reliability. Deep neural network schemas exhibit low bias along with high variance; the common approach of handling the variance problem is the employment of extra data. However, it is also known that data quality highly impacts the behavior of ML models. Poor performances are seen in out-of-distribution data instances and within heterogeneous regions of in-distribution data. Furthermore, datasets may contain labeling inconsistencies which can cause deceptions when training automated models for certain tasks. In the epilepsy use case, datasets suffer from a high imbalance between classes, where seizure events are short and rare when compared to the overall recordings.

We argue that by focusing on the quality of the data and by including representative cases in the training set, it is possible to achieve optimal performances within seizure detection frameworks. In contrast to task 1, the objective of task 2 is to apply data manipulation techniques in order to obtain the best performance (in terms of robustness and generalizability) of the provided model for wearable seizure detection.

In this task, participants will have access to the same training set as in task 1 and provided with a Deep Learning model. The model is an adapted version of the ChronoNet [2], a mixed convolutional and recurrent neural network composed of 1-D convolutional layers followed by a stack of gated recurrent units with skip connections. This framework was originally developed for abnormal EEG identification and has been adapted and optimized by the organizers for seizure detection. Participants are encouraged to apply any pre-processing techniques, data-augmentation, subsampling strategies, etc., in order to build a training set to feed the model.

The input segment size of the model is fixed at 2 second 2-channel EEG windows at a sampling frequency of 200 Hz [400 x 2]. The model’s architecture will be shared and the training routine cannot be changed by the participants. The model was implemented in python, with the use of the Keras API.
The output should be a vector of zeros (non-seizure) and ones (seizure) for each consecutive 2 second EEG segment. Both the **data processing and manipulation pipeline** and the **trained model’s weights** (serialize weights in HDF5 format) have to be submitted.

As a baseline, the metrics were computed with a model trained using all bhe-EEG seizure data segments of SeizeIT1 and randomly selected non-seizure data segments with a balancing factor of 10. The performance obtained was 58.22% sensitivity with a 117.12 false alarm rate (false alarms per hour).

&nbsp;  

### **<span style="color:#2B547E">Panel debate</span>**

What are useful EEG representations, and what can EEG signal processing look like in the AI era?![image](https://user-images.githubusercontent.com/53832320/205282151-a4518925-2fb1-426b-a44d-dcd98fe69bd3.png)

