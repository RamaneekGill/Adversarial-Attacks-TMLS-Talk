# Adversarial-Attacks-TMLS-Talk

Slides and code from my "Adversarial Attacks and their Impact on Insurance" talk at the Toronto Machine Learning Summit 2017 Nov.

## Overview

- Slides and notes are in `slides.pdf`
- First 75% of the literature review was documenteted, it is located in `literature review.pdf`
- Code is in `code/`
  - `dataset/` is missing in `src/` you can download it from here: [google drive link](https://drive.google.com/open?id=1Me5xS2mKtitjhMTYEI-4yiVFHQCE8wF9)
  - `dataset.zip` is ~200 MB and contains the inception net model used plus ~1000 test images
  - Code is in the format of a jupyter notebook
  - Both Python 3.x and 2.7.x work

## Installation

```
git clone https://github.com/RamaneekGill/Adversarial-Attacks-TMLS-Talk.git
cd Adversarial-Attacks-TMLS-Talk
pip install -r src/requirements.txt
jupyter notebook
```

## How to use the notebook

Dataset folder must be downloaded! Here is a link to the zipped folder: [google drive link](https://drive.google.com/open?id=1Me5xS2mKtitjhMTYEI-4yiVFHQCE8wF9)

- Specify file path image in `IMG_PATH` variable
- Specify the true label in `true_dict_index_pos` variable
  - If you don't know ignore this and look at the top prediction from the defence model further down in notebook
  - The label MUST exist in `code/dataset/ImageNet_labels.txt`
- Specify target label in `target_dict_index_pos`
  - The label MUST exist in `code/dataset/ImageNet_labels.txt`
- Specify type of attack in `ATTACK_TYPE` variable
  - A list of potential options are shown
  - Easy to extend and add your own
- Now you can run all the cells


Warning: If no target label is specified you may run into an error for some visualizations of heat maps