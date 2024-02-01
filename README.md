# ViewXGen

## Install
~~~
pip install -r requirements.txt
~~~

## Model Weights

####  1. [Chest X-ray Tokenizer](https://drive.google.com/file/d/1CqlKoZQb5FQPUzSk3zanKnFP0qFVSiWu/view?usp=sharing): Download VQGAN and place into the /mimiccxr_vqgan directory
####  2. [ViewXGen](https://drive.google.com/file/d/14GcInakobd0rIqt0HONMkLNHAINQI1ga/view?usp=drive_link): Download the model and place into the /ckpt directory

## Dataset

#### MIMIC-CXR
1. You must be a credential user defined in [PhysioNet](https://physionet.org/settings/credentialing/) to access the data.
2. Download chest X-rays from [MIMIC-CXR-JPG](https://physionet.org/content/mimic-cxr-jpg/2.0.0/) and reports from [MIMIC-CXR Database](https://physionet.org/content/mimic-cxr/2.0.0/)
3. We provide train, valid and test split sets in /metadata directory.


## Train Models

~~~
python unified_main.py
~~~

## Test Models

First, run unified_run.py. \
The generated discrete code sequences are saved as files.
  
~~~
python unified_run.py
~~~

#### For decoding chest X-rays,
Run decode_cxr.py. \
The generated seqeucens for chest X-rays are decoded and saved in the '.jpeg' format.

~~~
python decode_cxr.py
~~~
