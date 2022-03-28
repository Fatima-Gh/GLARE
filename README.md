[![CC BY 4.0][cc-by-shield]][cc-by]


# GLARE: Google Apps Arabic Reviews



Dataset and Code of "GLARE: Google Apps Arabic Reviews" paper submitted to International Conference on Language Resources and Evaluation (LREC) 2022 to The 5th Workshop on Open-Source Arabic Corpora and Processing Tools (OSACT).


You can download the paper via: [[Github]](xx.pdf) [[DOI]](https://doi.org/xx/xx) [[ArXiv]](https://arxiv.org/abs/xxxx.xxxxx) [[PapersWithCode]](https://paperswithcode.com/).

## Paper Summary

[Summarize your work in one sentence]

## Preparation
### Below is details about each file, please ensure that you have enough storage before downloading the data.

| Data Type         | File Name  | File Size | File Type |
| ------------------ |---------------- | -------------- |-------------- |
| raw   |     apps        |      3.9 MB       | CSV |
| raw   |     reviews        |      95%       | CSV |
| raw   |     categories        |      95%       | CSV
| engineered   |     apps        |      3.9 MB       | CSV
| engineered   |     reviews        |      95%       | CSV
| engineered   |     vocabulary        |      530.5 MB       | CSV

## File Specifications

- **apps.csv**: File that contains apps metadata.
- **reviews.csv**: File that contain reviews and reviews metadata.
- **categories/**: Folder that contains 59 csv files, each file corrospond to one category with apps and apps metadata scrapped from top 200 free apps for that category.
- **vocabulary.csv**: File that contains vocabulary set generated from reviews with additional engineered features (word length, word frequency, has noise or digits, ..etc.)


### Raw Data
### Apps Metadata
| title         | appId  | url | icon | developer | developerId | summary | score |
| ------------------ |---------------- | -------------- |-------------- | ------------------ |---------------- | -------------- |-------------- |
| application name/title   |      application unique identifier        |      application url at Google PlayStore    | url for image object  | developer name | developer unique identifier | short description of the application | application accumlated rating |  

### Reviews Metadata


| at         | content  | repliedAt | replyContent | reviewCreatedVersion | reviewId | score | thumbsUpCount | userImage | userName | appID |
| ------------------ |---------------- | -------------- |-------------- | ------------------ |---------------- | -------------- |-------------- |---------------- | -------------- |-------------- |
| datetime   |     review text        |      developers reply time      | developers reply content | application version during the time of review | unique ID for each review  |     user rating        |      number of users that agree with the reviewer       | url for image object | user display name   |     application unique identifier        |  


### Engineered Data

### Apps Metadata
Same as apps.csv in raw data with the following additions:

| at         | content  | repliedAt | replyContent | reviewCreatedVersion | reviewId | score | thumbsUpCount | userImage | userName | appID |
| ------------------ |---------------- | -------------- |-------------- | ------------------ |---------------- | -------------- |-------------- |---------------- | -------------- |-------------- |
| datetime   |     review text        |      developers reply time      | developers reply content | application version during the time of review | unique ID for each review  |     user rating        |      number of users that agree with the reviewer       | url of image object | user display name   |     application unique identifier        |  

### Reviews Metadata
Same as reviews.csv in raw data with the following additions:


| at         | content  | repliedAt | replyContent | reviewCreatedVersion | reviewId | score | thumbsUpCount | userImage | userName | appID |
| ------------------ |---------------- | -------------- |-------------- | ------------------ |---------------- | -------------- |-------------- |---------------- | -------------- |-------------- |
| datetime   |     review text        |      developers reply time      | developers reply content | application version during the time of review | unique ID for each review  |     user rating        |      number of users that agree with the reviewer       | url of image object | user display name   |     application unique identifier        |  

### Folders Structure

- Data are prepared as raw data or engineered data.
- Download the dataset files [Google Drive](https://example.com) | [Zenodo](https://example.com) | [Google Drive](https://example.com).
- The directory structure is as follows:
```
data
└── raw
   ├── apps.csv
   ├── reviews.csv
   └── categories/
└── engineered
   ├── apps.csv
   ├── reviews.csv
   └── vocabulary.csv
```

## Usage

### Starter Code:

```bash
python main.py --arg1 arg1 --arg2 arg2
```

## Citation

If you use this dataset please cite as:

```bibtex
@inproceedings{[author_first_name][year][abbr],
  title={[paper title]},
  author={[authors]},
  booktitle={[venue]},
  year={[year]}
}
```

## Acknowledgments

This work is supported by National Center for Artificial Intelligence - SDAIA.

## Contact

[Fatima AlGhamdi](fatima.alghamdi@hotmail.com)

## License

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
