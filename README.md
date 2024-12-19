---
license: odc-by
dataset_info:
- config_name: finemath-3plus
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
    num_bytes: 137764105388.93857
    num_examples: 21405610
  download_size: 65039196945
  dataset_size: 137764105388.93857
- config_name: finemath-4plus
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
    num_bytes: 39101488149.09091
    num_examples: 6699493
  download_size: 18365184633
  dataset_size: 39101488149.09091
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
    num_bytes: 96485696853.10182
    num_examples: 13882669
  download_size: 46808660851
  dataset_size: 96485696853.10182
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
    num_bytes: 40002719500.1551
    num_examples: 6296212
  download_size: 19234328998
  dataset_size: 40002719500.1551
configs:
- config_name: finemath-3plus
  data_files:
  - split: train
    path: finemath-3plus/train-*
- config_name: finemath-4plus
  data_files:
  - split: train
    path: finemath-4plus/train-*
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

* `finemath-3plus`: FineMath (English) with `int_score >= 3`
* `finemath-4plus`: FineMath (English) with `int_score >= 4`
* `infiwebmath-3plus`: Infi-WebMath (English-only) with `int_score >= 3`
* `infiwebmath-4plus`: Infi-WebMath (English-only) with `int_score >= 4`

```python
from datasets import load_dataset
data = load_dataset("HuggingFaceTB/finemath", "finemath-4plus", split="train", num_proc=8)
```