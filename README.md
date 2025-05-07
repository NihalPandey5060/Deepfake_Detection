# DeepFake-Analysis ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=000) ![Django](https://img.shields.io/badge/Django-%23092E20.svg?logo=django&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff) 

## Introduction

This repository contains a project for DeepFake Image Detection. The project is divided into two parts:

### Development of a DeepFake Image Detection Model

- Inspired by "[An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)" by Dosovitskiy et al. (2020). The Vision Transformer model is used for transfer learning on the DeepFake Detection Dataset.

- A subset of Open Forensics Dataset ([Deepfake Dataset](https://www.kaggle.com/datasets/manjilkarki/deepfake-and-real-images/data)) consisting of approx. 1.9 million images is used for training the model. The dataset is divided into 3 sets: Training, Validation, and Testing Sets with a 14:4:1 ratio. Transfer Learning is used to train the model to detect DeepFake Images.

- The model trained is then deployed onto Hugging Face Model Hub for public use. The model is available for use at: [DeepFake Image Detection Model](https://huggingface.co/sakshamkr1/deepfake_vit)

## Model Statistics

- Achieved an accuracy of 97% on the Testing Set.
- Model trained on Azure ML Studio notebooks, with a compute VM of 16 Core, 128 GB RAM for a period of 6 hours.


## Web Application

- The Web Application is developed using Django Framework.
- The Web Application retrieves the image from the user via a user-friendly interface. During deployment, the model is retrieved from the Hugging Face Model Hub via the API, hence the user does not need to download the model in the project directory.
- The Web Application can be further deployed on Azure App Services for public use.

## App Demo

.....




## [Combating Digitally Altered Images: Deepfake Detection- Microsoft Tech Community's Educator Blog](https://techcommunity.microsoft.com/blog/educatordeveloperblog/combating-digitally-altered-images-deepfake-detection/4401278?wt.mc_id=studentamb_217334) 

## Installation and Usage

- Clone the repository using the following command:

    ```bash
    git clone https://github.com/Polymath-Saksh/deepfake.git
    ```

- Install the required dependencies using the following command:

    ```bash
    pip install -r requirements.txt
    ```

- Run the Django Server using the following command:

    ```bash
    python manage.py runserver
    ```


- [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929) by Dosovitskiy et al. (2020) for the Vision Transformer Model.

