# EEG Signal Processing for Eye Tracking

## It's a summary of the paper with my opinions

## Published
- Conference: Signal Processing Conference (EUSIPCO), 2014 Proceedings of the 22nd European. Publisher: IEEE

## Abbriviations
**VOG** : Video Oculography
**EOG** : Electro Occulography
**SSVEP** : Steady State visually invoked potential
**ICA** : Independent Component Analysis
**BCI** : Brain-Computer interface

## VOG
VOG data has noise and it varies depending on lighting conditions, distance between Eye and camera. 
## EOG (Non-Optical method to track eye)
EOG provides two additional eye movement information sources:
- Occulomuscular movements via EOG
- Brain's response to flickering stimuli: SSVEP
This 2 are combined for the EEG Eye tracking solution 

## Eye tracking can be defined by followings
- Person's focus of foveal attension 
- eye movement types (saccades, smooth pursuits, fixation, blinking)

## Artefacts of EOG (Noise)
- Environmental
- Biological 

## ICA for feature extraction
As EOG has artefacts and normal Average filtering, LR methoeds cannot compansate them easily. With help if ICA (A blind source seperation method) it can be better. ICI takes all EGG signals as mixture of independent signals. It can find signal characterstics such as Entropy, mitual informations

## SSVEP
It's an electrical response in the brain when the retina is simulated by flickering visual stimulus (when freq>6hz). It's useful to estimate a person't Focus of Attension. (when the focus is flickering)

## Signal Processing
- Preprocessing: Band-Pass Filtered to remove the slow drifts and High Frequency noise
- Feature Extraction: Features are extracted from pre-processed EOG signals. Power Spectical Density is estimated with Welch's method.
- ICA: Used algo: Extended Informax
## Classification
- KNN
- for eye movement 4 classes (blink, fixation, saccade, pursuit)
- for SSVEP 4 classes (0Hz, 7Hz, 10Hz, 12Hz)
- Performance measurement: RMSE (Root Mean Square Error)
## Session inteface
- 9 points in 9 corner of the monitor. (My opinion: An inteface like Webgazer)

## Result
![result]('pictures/result.PNG')