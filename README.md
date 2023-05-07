# RPNet

This code is based on the work done in "A Deep Learning approach for robust R Peak detection in noisy ECG". The trained model has been utilised with the dataset I gathered to determine the accurarcy of this method in predicting emotions based on heart rhythm. This method is compared against detrending method to detect peaks from basic UWB radar data.
## Research

### Architecture Diagram

<p align="center">
  <image src = 'imgs/Unet_5.png' >
</p>

### Datasets (for training)

[Chinese Physiological Signal Challenge (CPSC 2019)](http://2019.cpscsub.com/)

### Quantitative Comparisons
Evaluation of model and three traditional methods on CPSC dataset

<p align="center">
  <image src = 'imgs/CPSC_eval.png' >
</p>

Evalation of Model on the other 3 datasets

<p align="center">
  <image src = 'imgs/Perf_on_3_datasets.png' >
</p>

Evaluation of Model in presence of noise(SNR wise) on NSTDB

<p align="center">
  <image src = 'imgs/Perf_on_NSTDB.png' >
</p>

### Qualitative Results
<p align="center">
  <image src = 'imgs/Collage_results.png' >
</p>

### Steps 

-- General Steps
* Download all the 4 datasets.

-- To train the model
* Run train_CPSC.ipynb

-- To Evaluate the model
* [Download the model](https://drive.google.com/file/d/19xN7pZsALb09bxWjrSKdAlJmRqYL0M0g/view?usp=sharing)
* To evaluate on CPSC: `sh evaluate_detectors_CPSC.sh`
* To evaluate on any one of the other three datasets: `sh evaluate_detectors_CPSC.sh`
* To evaluate on the NSTDB dataset: `sh evaluate_nstdb.sh` 

Details on possible changes that can be made to the scipt will be mentioned in the script. We would like to acknowledge Mr Bernd Porr whose repo we forked for the [implementation](https://github.com/berndporr/py-ecg-detectors) of the traditional ECG Detectors.
