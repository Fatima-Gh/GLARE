# GLARE: Google Apps Arabic Reviews

Dataset and Code of "GLARE: Google Apps Arabic Reviews" paper submitted to International Conference on Language Resources and Evaluation (LREC) 2022 to The 5th Workshop on Open-Source Arabic Corpora and Processing Tools (OSACT).
You can download the paper via: [[Github]](xx.pdf) [[DOI]](https://doi.org/xx/xx) [[ArXiv]](https://arxiv.org/abs/xxxx.xxxxx) [[PapersWithCode]](https://paperswithcode.com/).

## One-Sentence Summary

[Summarize your work in one sentence]

![Insert a preview image here](https://via.placeholder.com/300.jpg)


## Preparation
### Below is each file size, please ensure that you have enough storage before downloading the data.

| Data Type         | File Name  | File Size | File Type |
| ------------------ |---------------- | -------------- |-------------- |
| raw   |     apps        |      3.9 MB       | CSV |
| raw   |     reviews        |      95%       | CSV |
| raw   |     categories        |      95%       | CSV
| engineered   |     apps        |      3.9 MB       | CSV
| engineered   |     reviews        |      95%       | CSV
| engineered   |     vocabulary        |      530.5 MB       | CSV

### Prepare the training data:

- Data are prepared as raw data or engineered data.
- Download the dataset files [Google Drive](https://example.com) | [Google Drive](https://example.com) | [Google Drive](https://example.com).
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

### Training:

```bash
python main.py --arg1 arg1 --arg2 arg2
```

### Evaluation:

```bash
python main.py --evaluate --arg1 arg1 --arg2 arg2
```

## File Specifications

- **app.csv**: Description for the model architecture.
- **reviews.csv**: Used functions for data preprocessing.
- …

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

This work is supported by [funds].

## Contact

[Email address of the corresponding contributor]

## License

[License]
