---
license: odc-by
dataset_info:
- config_name: finemath-scratch-3plus
  features:
  - name: url
    dtype: string
  - name: fetch_time
    dtype: int64
  - name: content_mime_type
    dtype: string
  - name: warc_filename
    dtype: string
  - name: warc_record_offset
    dtype: int32
  - name: warc_record_length
    dtype: int32
  - name: text
    dtype: string
  - name: token_count
    dtype: int32
  - name: char_count
    dtype: int32
  - name: metadata
    dtype: string
  - name: score
    dtype: float64
  - name: int_score
    dtype: int64
  - name: crawl
    dtype: string
  - name: snapshot_type
    dtype: string
  - name: language
    dtype: string
  - name: language_score
    dtype: float64
  splits:
  - name: train
    num_bytes: 137776842011
    num_examples: 21407589
  download_size: 64839987399
  dataset_size: 137776842011
- config_name: finemath-scratch-4plus
  features:
  - name: url
    dtype: string
  - name: fetch_time
    dtype: int64
  - name: content_mime_type
    dtype: string
  - name: warc_filename
    dtype: string
  - name: warc_record_offset
    dtype: int32
  - name: warc_record_length
    dtype: int32
  - name: text
    dtype: string
  - name: token_count
    dtype: int32
  - name: char_count
    dtype: int32
  - name: metadata
    dtype: string
  - name: score
    dtype: float64
  - name: int_score
    dtype: int64
  - name: crawl
    dtype: string
  - name: snapshot_type
    dtype: string
  - name: language
    dtype: string
  - name: language_score
    dtype: float64
  splits:
  - name: train
    num_bytes: 39107231250
    num_examples: 6700477
  download_size: 18312712924
  dataset_size: 39107231250
- config_name: infiwebmath-3plus
  features:
  - name: url
    dtype: string
  - name: metadata
    dtype: string
  - name: score
    dtype: float64
  - name: int_score
    dtype: int64
  - name: token_count
    dtype: int64
  - name: char_count
    dtype: int64
  - name: text
    dtype: string
  splits:
  - name: train
    num_bytes: 96495948225
    num_examples: 13884144
  download_size: 46639785362
  dataset_size: 96495948225
- config_name: infiwebmath-4plus
  features:
  - name: url
    dtype: string
  - name: metadata
    dtype: string
  - name: score
    dtype: float64
  - name: int_score
    dtype: int64
  - name: token_count
    dtype: int64
  - name: char_count
    dtype: int64
  - name: text
    dtype: string
  splits:
  - name: train
    num_bytes: 43765365410.18643
    num_examples: 6297100
  download_size: 19238942936
  dataset_size: 43765365410.18643
configs:
- config_name: finemath-scratch-3plus
  data_files:
  - split: train
    path: finemath-scratch-3plus/train-*
- config_name: finemath-scratch-4plus
  data_files:
  - split: train
    path: finemath-scratch-4plus/train-*
- config_name: infiwebmath-3plus
  data_files:
  - split: train
    path: infiwebmath-3plus/train-*
- config_name: infiwebmath-4plus
  data_files:
  - split: train
    path: infiwebmath-4plus/train-*
---


Data subsets:

* `finemath-scratch-3plus`: FineMath (English) with `int_score >= 3`
* `finemath-scratch-4plus`: FineMath (English) with `int_score >= 4`
* `infiwebmath-3plus`: Infi-WebMath (English-only) with `int_score >= 3`
* `infiwebmath-4plus`: Infi-WebMath (English-only) with `int_score >= 4`

```python
from datasets import load_dataset
data = load_dataset("swissai-hf-data/finemath", "finemath-scratch-4plus", split="train", num_proc=8)
```