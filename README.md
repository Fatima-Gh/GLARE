[![CC BY 4.0][cc-by-shield]][cc-by]
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6457824.svg)](https://doi.org/10.5281/zenodo.6457824)


# GLARE: Google Apps Arabic Reviews



Dataset and Code of "GLARE: Google Apps Arabic Reviews" paper.


You can access the paper via: [arxiv](https://arxiv.org/abs/2412.15259)


## Paper Summary

We introduce GLARE: Google Apps Arabic Reviews dataset. A collection of 76M reviews from 9,980 Android apps collected from Google PlayStore Saudi store.

## Preparation
#### Below is details about each file, please ensure that you have enough storage before downloading the data.

| Data Type         | File Name  | File Size | File Type |
| ------------------ |---------------- | -------------- |-------------- |
| raw   |     apps        |      4.1 MB       | CSV |
| raw   |     reviews        |      17 GB      | CSV |
| raw   |     categories/        |      4.3 MB       | CSV
| engineered   |     apps        |      3.8 MB       | CSV
| engineered   |     reviews        |      21.9 GB       | CSV
| engineered   |     vocabulary        |      530.5 MB       | CSV

## File Specifications

- **apps.csv**: File that contains apps metadata.
- **reviews.csv**: File that contains reviews and reviews metadata.
- **categories/**: Folder that contains 59 CSV files, each file corrosponds to one category with apps and apps metadata scrapped from top 200 free apps for that category.
- **vocabulary.csv**: File that contains vocabulary set generated from reviews with additional engineered features (word length, word frequency, has noise or digits, ..etc.)


### Raw Data
#### Apps Metadata

```
{
    "title":"application name/title",
    "app_id":"application unique identifier",
    "url":"application url at Google PlayStore",
    "icon":"url for image object",
    "developer":"developer name",
    "developer_id":"developer unique identifier",
    "summary":"short description of the application",
    "rating":"application accumulated rating"
 }
 ```

#### Reviews Metadata

```

{
   "at":"review datetime",
   "content":"review text",
   "replied_at":"developer reply datetime",
   "reply_content":"developer reply content",
   "review_created_version":"user application version during the time of review",
   "review_id":"review unique identifier",
   "rating":"user rating",
   "thumbs_up_count":"number of users that agree with the reviewer",
   "user_name":"user display name",
   "app_id":"application unique identifier"
}


```
### Engineered Data

#### Apps Metadata
Same as apps.csv in raw data with the following additions:

```
{
   "reviews_count":"number of reviews for the application",
   "categories":"list of application categories",
   "categories_count":"number of application categories"

}
```

#### Reviews Metadata
Same as reviews.csv in raw data with the following additions:

```

{
  "tokenized_review":"list of review words tokenized on white-space",
  "words_count":"number of words in review"
}


``` 


#### Vocabulary 

```

{
   "word":"term text",
   "length":"word characters count",
   "frequency":"word occurrences in the reviews dataset",
   "has_noise":"true or false if word contains anything non-arabic alphanumeric",
   "noise":"list of noise (anything non-arabic alphanumeric) in the word",
   "has_digits":"true or false if word contains arabic or hindi digits",
   "digits":"list of digits in the word"
}


``` 


### Folders Structure

- Data are prepared as raw data or engineered data.
- Download the dataset files: [Google Drive](https://drive.google.com/drive/folders/1Cb61K3wFdVlIQfKouchsUpn5oXdJbhyg?usp=sharing) | [Zenodo](https://zenodo.org/record/6457824#.Ylv-gX9Bz8w) | [Alternative Google Drive](https://drive.google.com/drive/folders/1jWCCyJPKFf6Q-1zDuGRUBi6XtlmkyHlt?usp=sharing)
- The directory structure is as follow:
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
<!-- 
## Usage

### Starter Code:

```bash
python main.py --arg1 arg1 --arg2 arg2
```
 -->
## Citation

If you use this dataset please cite as:

```bibtex
@dataset{alghamdi_fatima_2022_6457824,
  author       = {AlGhamdi, Fatima and
                  Mohammed, Reem and
                  Al-Khalifa, Hend and
                  Alowisheq, Areeb},
  title        = {GLARE: Google Apps Arabic Reviews Dataset},
  month        = apr,
  year         = 2022,
  publisher    = {Zenodo},
  version      = {1.0},
  doi          = {10.5281/zenodo.6457824},
  url          = {https://doi.org/10.5281/zenodo.6457824}
}

```

<!--
```
AlGhamdi, Fatima, Mohammed, Reem, Al-Khalifa, Hend, & Alowisheq, Areeb. (2022). GLARE: Google Apps Arabic Reviews Dataset (1.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.6457824
```


```bibtex
@inproceedings{[author_first_name][year][abbr],
  title={[paper title]},
  author={[authors]},
  booktitle={[venue]},
  year={[year]}
}
```
-->
<!-- ## Acknowledgments

This work is supported by National Center for Artificial Intelligence - SDAIA.

## Contact

[Fatima AlGhamdi](fatima.alghamdi@hotmail.com) -->

## License

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
