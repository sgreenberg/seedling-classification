# seedling-classification

My Capstone Project for Udacity's Machine Learning nanodegree will attempt to classify twelve different species of plants by image analysis. This project will utilize the dataset from [Kaggle's Plant Seedlings Identification](https://www.kaggle.com/c/plant-seedlings-classification) competition.

# Setup

1. Download training images, test images. Folder structure should look like this: 

```
  seedling-classification
    - data
      - train
        - Black-grass
           - 0ace21089.png
             ...
        - Charlock
        ...
      - test
        - 0a64e3e6c.png
        ...
```

2. To do. Bottleneck features!!!

3. (Optional) __If you plan to use GPUs__, install the necessary NVIDIA software on your system. I followed [this guide](https://github.com/GoogleCloudPlatform/ml-on-gcp/blob/master/gce/survival-training/README-tf-estimator.md) to set up GPUs on a Google Compute Engine instance.

4. Install anaconda if you don't have it already.

  ```
  wget https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh
  bash Anaconda3-5.0.1-Linux-x86_64.sh
  source ~/.bashrc
  ```

4. Create (and activate) a new environment.

  - __Linux__ (to install with __GPU support__, change `requirements/linux.yml` to `requirements/linux-gpu.yml`): 
  ```
  conda env create -f requirements/linux.yml
  source activate seedlings
  ```
  - __Mac__ (to install with __GPU support__, change `requirements/mac.yml` to `requirements/mac-gpu.yml`): 
  ```
  conda env create -f requirements/mac.yml
  source activate seedlings
  ```

  
5. Switch [Keras backend](https://keras.io/backend/) to TensorFlow.
  ```
  KERAS_BACKEND=tensorflow python -c "from keras import backend"
  ```

6. Open the notebook.
```
jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser seedlings.ipynb
```

# Acknowledgements

Setup Instructions taken from [Udacity's CNN dog-project](https://github.com/udacity/dog-project)