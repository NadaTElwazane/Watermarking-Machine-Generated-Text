# Watermarking Machine-Generated Text
This repository contains the code for our senior project "Watermarking Machine-Generated Text".
<!-- create a table with notebooks and Datasets as header -->

## **No Attacks**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Create a dataset of Unwatermarked Text | [Notebook](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Unwatermarked/create-unwatermarked-dataset.ipynb) | [Dataset](./Datasets/No%20Attacks/Unwatermarking/generated_texts.csv) |
| 2. Test Watermarking and Detection Algorithms| [Logits Deviation with Green-Red List](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/logits-deviation-with-green-red-list-v1-FAIL.ipynb) <br>  [Sampling With Randomized Numbers using TinyLlama](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/sampling-with-randomized-numbers-TinyLlama.ipynb) <br>  [Logits Deviation with Randomized Numbers using OPT-350M](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/sampling-with-randomized-opt-350m.ipynb) | N/A |
| 3. Automate Watermarking Using the [Sunbird Dataset](https://www.kaggle.com/datasets/mekaneeky/sunbird-english-prompts)   |  [Part 1](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-1.ipynb) <br>  [Part 2](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-2.ipynb) <br>  [Part 3](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-3.ipynb) <br>  [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-watermarked-text-dataset.ipynb)| [Part 1](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-1.csv) <br> [Part 2](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-2.csv) <br> [Part 3](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-3.csv) <br> [Merged](./Datasets/No%20Attacks/Merged/merged-watermarked-and-unwatermarked-text.csv) |
| 4. Merge Unwatermarked and Watermarked Datasets | [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-watermarked-and-unwatermarked-dataset.ipynb) <br> [Truncate](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-truncated-watermarked-and-unwatermarked-dataset.ipynb) | [Merged](./Datasets/No%20Attacks/Merged/merged-watermarked-and-unwatermarked-text.csv) <br> [Truncated](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv) |
| 5. Run the Detection Algorithm on the first 1200 rows of the Truncated Dataset | [Part1](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-1.ipynb) <br> [Part2](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-2.ipynb) <br> [Part3](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-3.ipynb) <br> [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-pvalue-scores-dataset.ipynb)| [Part1](./Datasets/No%20Attacks/Detection/p-value-label-part-1.csv) <br> [Part2](./Datasets/No%20Attacks/Detection/p-value-label-part-2.csv) <br> [Part3](./Datasets/No%20Attacks/Detection/p-value-label-part-3.csv) <br> [Merged](./Datasets/No%20Attacks/Merged/merged-p-value-label.csv) |
| 6. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm | [Notebook](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/evaluate-the-detection-algorithm.ipynb) | N/A |

## **Simulating Attacks**
### **1. Paraphrasing Attack**
| Description | Notebooks | Datasets |
| --- | --- | --- |
|1. Experimented paraphrasing using Dipper | [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/Dipper/Dipper%20-%20v1.ipynb) | N/A |
|2. Experimented paraphrasing using T5 on the [Watermarked Dataset](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv)| [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/T5/t5-generated-text-and-paraphrased-only.ipynb) | [Dataset](./Datasets/Attacks/Paraphrasing%20attack/paraphased-text.csv) |
|3. Run the Detection Algorithm on the [Paraphrased Dataset](./Datasets/Attacks/Paraphrasing%20attack/paraphased-text.csv) | [Part1](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/detection-paraphrased-part-1.ipynb) <br> [Part2](.) <br> [Part3](./) <br> [Merge](.)| [Part1](./Datasets/Attacks/Paraphrasing%20attack/Detection/paraphrasing_test_results-part%201.csv) <br> [Part2](.) <br> [Part3](.) <br> [Merged](.) |




---
## **Evaluating LLM With and Without Watermark**
***EXPERIMENTAL***
| Description | Notebooks | Datasets |
| --- | --- | --- |
|1. Evaluate OPT-350M (No Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [MCQ FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt-350m-mcq-hellaswag-v1.ipynb) <br> [Auto-Complete FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt-350m-autocomplete-hellaswag-v1.ipynb)<br>[Minimum Loss](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-loss-v1.ipynb) | N/A |
|***FAILED & ABANDONED*** Evaluate GEMMA-2B (No Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [MCQ and Auto-Complete FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/gemma-mcq-and-autocomplete-v1-FAIL.ipynb) | N/A |
|2. Evaluate OPT-350M (With Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [Logits with Red-Green List (Minimum Loss) FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt350m-evaluating-a-watermark-for-llm-fail-v1.ipynb)| N/A |