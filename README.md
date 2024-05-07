# DLH598-Team144, Detecting Heart Disease from Multi-View Ultrasound Images via Supervised Attention Multiple Instance Learning

This repo provides a Jupyter notebook that can be used to reproduce the results of the academic paper, Detecting Heart Disease from Multi-View Ultrasound Images via Supervised Attention Multiple Instance Learning, from Huang et. al.

The original paper can be viewed [here](https://arxiv.org/abs/2306.00003), and the original repo can be found [here](https://github.com/tufts-ml/SAMIL/tree/main). You can view a brief overview of the reproduction [here](https://www.youtube.com/watch?v=mZLC0L0FTKQ).

This notebook was developed in Google Colab with the Pro+ subscription to enable access to Nvidia A100's for training and access to Google Drive. You can choose to run this notebook in Google Colab, or modify the notebook to pull files locally instead of from Google Drive.

### Setup Steps

To use this notebook, the following steps MUST be followed:

1. Apply for access to the TMED-2 dataset here: https://tmed.cs.tufts.edu/data_access.html
2. Upload the TMED-2 dataset's `labeled.zip` and `unlabeled.zip` from the `view_and_diagnosis_labeled_set` to your Google Drive (or locally) and set the `DATA_DIR` global variable in the notebook to point to your dataset location. Failure to do so will results in errors. Remove the Google Drive mounting line if only using a local dataset (`drive.mount('/content/drive', force_remount=True)`) and the import `from google.colab import drive`.
3. Run each code cell in order.

If you are not running the notebook in Google Colab, the following packages are required. Please install them prior to execution:

- numpy
- pandas
- matplotlib
- pytorch
- torchvision
- tqdm
- sklearn

### Computational Requirements

The results in the notebook were produced with an Nvidia A100 GPU. Training time was between 2-3 hours per model variant with a single A100 GPU. It is highly recommended to use an A100 or equivalent, such as a 4080 or 4090 for training in a reasonable amount of time.

### Pretrained Models
- SAMIL with Study Level Pretraining: https://drive.google.com/uc?id=1-860ddmCB0_Kq8EIO-DLfHEi0yB-4K0w
- SAMIL with Image Level Pretraining: https://drive.google.com/uc?id=166uyrtMb0joJA3ETVG0sF5OIHRDZTTy3
- SAMIL with No Pretraining: https://drive.google.com/uc?id=1-BYHiZ7iefhl9xI2TNt3Egnk2rjrJdAq
- ABMIL: https://drive.google.com/uc?id=1-HQQIBXXPrKh7N8kobyPJe5FQ8Ov6vO2

### Citation
@misc{huang2021new, title={A New Semi-supervised Learning Benchmark for Classifying View and Diagnosing Aortic Stenosis from Echocardiograms}, author={Zhe Huang and Gary Long and Benjamin Wessler and Michael C. Hughes}, year={2021}, eprint={2108.00080}, archivePrefix={arXiv}, primaryClass={cs.CV} }

@misc{huang2024detecting, title={Detecting Heart Disease from Multi-View Ultrasound Images via Supervised Attention Multiple Instance Learning}, author={Zhe Huang and Benjamin S. Wessler and Michael C. Hughes}, year={2024}, eprint={2306.00003}, archivePrefix={arXiv}, primaryClass={eess.IV} }
