# CE7454_Project_Fall2018_NTU

[![Binder](https://mybinder.org/badge.svg)][binder]

[binder]: https://mybinder.org/v2/gh/Lukeeeeee/CE7454_Project_Fall2018_NTU/master
CE7454 Project for Deep Learning for Data Science Fall 2018 NTU

![](./report_fig/result1.png)


### Environment Set-up

```bash
git clone https://github.com/Lukeeeeee/CE7454_Project_Fall2018_NTU
cd CE7454_Project_Fall2018_NTU
conda env create environment.yml
source activate dlproject
```

### Download dataset

1. Install [kaggle API](https://github.com/Kaggle/kaggle-api): `pip install kaggle`
3. Create API token from `https://www.kaggle.com/<username>/account` and save the file to `~/.kaggle/kaggle.json` 
4. Download the Carvana dataset: `kaggle competitions download -c carvana-image-masking-challenge`
5. Unzip the dataset into to `train.csv` `valid.csv` `test.csv`
  
### Running the crawler

```bash
cd crawler
scrapy crawl cars
```

### Download the trained models

The trained model by initializing weight with restored weights an with non-augmentation is available in [here](https://entuedu-my.sharepoint.com/:u:/g/personal/wei005_e_ntu_edu_sg/EeQC4kIQGzhPt0UFK4Azmg8B3afFElqIVEc-xUeHO5hvBQ?e=viVIFu
) (you may try this as evaluation first):

The other trained models are avaliable in [here](https://entuedu-my.sharepoint.com/:u:/g/personal/wei005_e_ntu_edu_sg/Eboz72eW3MBLuOywT7RQyJwBcbaYt5KclrNwe7DH-qg7Pw?e=iIqQH0)

### Inference Stage
Several params:

```bash
--model_log_dir the trained model path
--check_point check point of your model
--mode inference in default
--img_path the single image you'd like to test on this trained model
(submission should be false in this case)
--submit true if you'd like to go through the whole kaggle dataset
```
