# Watermarking Machine-Generated Text
This repository contains the code for our senior project "Watermarking Machine-Generated Text".

|Final Notebook|
|---|
 [Notebook](./Notebooks/generation-and-detection-all-attacks-v1.ipynb)|

## **No Attacks**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Create a dataset of Unwatermarked Text | [Notebook](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Unwatermarked/create-unwatermarked-dataset.ipynb) | [Dataset](./Datasets/No%20Attacks/Unwatermarking/generated_texts.csv) |
| 2. Test Watermarking and Detection Algorithms| [Logits Deviation with Green-Red List](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/logits-deviation-with-green-red-list-v1-FAIL.ipynb) <br>  [Sampling With Randomized Numbers using TinyLlama](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/sampling-with-randomized-numbers-TinyLlama.ipynb) <br>  [Logits Deviation with Randomized Numbers using OPT-350M](./Notebooks/No%20Attacks/Manual%20Watermarking%20and%20Detection/sampling-with-randomized-opt-350m.ipynb) | N/A |
| 3. Automate Watermarking Using the [Sunbird Dataset](https://www.kaggle.com/datasets/mekaneeky/sunbird-english-prompts)   |  [Part 1](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-1.ipynb) <br>  [Part 2](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-2.ipynb) <br>  [Part 3](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Watermarking/create-watermarked-dataset-part-3.ipynb) <br>  [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-watermarked-text-dataset.ipynb)| [Part 1](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-1.csv) <br> [Part 2](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-2.csv) <br> [Part 3](./Datasets/No%20Attacks/Watermarking/watermarked-texts-part-3.csv) <br> [Merged](./Datasets/No%20Attacks/Merged/merged-watermarked-and-unwatermarked-text.csv) |
| 4. Merge Unwatermarked and Watermarked Datasets | [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-watermarked-and-unwatermarked-dataset.ipynb) <br> [Truncate](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-truncated-watermarked-and-unwatermarked-dataset.ipynb) | [Merged](./Datasets/No%20Attacks/Merged/merged-watermarked-and-unwatermarked-text.csv) <br> [Truncated](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv) |
| 5. Run the Detection Algorithm on the first 1200 rows of the Truncated Dataset | [Part1](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-1.ipynb) <br> [Part2](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-2.ipynb) <br> [Part3](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/create-pvalue-scores-dataset-part-3.ipynb) <br> [Merge](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Merge%20Datasets/create-merged-pvalue-scores-dataset.ipynb)| [Part1](./Datasets/No%20Attacks/Detection/p-value-label-part-1.csv) <br> [Part2](./Datasets/No%20Attacks/Detection/p-value-label-part-2.csv) <br> [Part3](./Datasets/No%20Attacks/Detection/p-value-label-part-3.csv) <br> [Merged](./Datasets/No%20Attacks/Merged/merged-p-value-label.csv) |
| 6. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm | [Notebook](./Notebooks/No%20Attacks/Automated%20Watermarking%20and%20Detection/Detection/evaluate-the-detection-algorithm.ipynb) | N/A |

## **Simulating and Counteracting Attacks**
### **1. Paraphrasing Attack**
| Description | Notebooks | Datasets |
| --- | --- | --- |
|1. Experimented paraphrasing using Dipper | [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/Dipper/Dipper%20-%20v1.ipynb) | N/A |
|2. Experimented paraphrasing using T5 on the [Watermarked Dataset](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv)| [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/T5/t5-generated-text-and-paraphrased-only.ipynb) | [Dataset](./Datasets/Attacks/Paraphrasing%20attack/paraphased-text.csv) |
|3. Run the Detection Algorithm on the [Paraphrased Dataset](./Datasets/Attacks/Paraphrasing%20attack/paraphased-text.csv) | [Part1](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/detection-paraphrased-part-1.ipynb) <br> [Part2](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/detection-paraphrased-part2.ipynb) <br> [Part3](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/detection-paraphrased-part3.ipynb) <br> [Merge](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/merge-detection-paraphrased.ipynb)| [Part1](./Datasets/Attacks/Paraphrasing%20attack/Detection/paraphrasing_test_results-part%201.csv) <br> [Part2](./Datasets/Attacks/Paraphrasing%20attack/Detection/paraphrasing_test_results-part%202.csv) <br> [Part3](./Datasets/Attacks/Paraphrasing%20attack/Detection/paraphrasing_test_results-part3.csv) <br> [Merged](./Datasets/Attacks/Paraphrasing%20attack/Detection/merged-data-paraphrasing-detection.csv) |
|4. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm after Paraphrasing| [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/Detection/evaluate-model-after-paraphrasing.ipynb) | N/A |
|5. Experimented paraphrasing using Roundtrip paraphrasing (English to French to English) on the [Watermarked Dataset](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv)| [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/RT%20paraphrasing/roundtrip.ipynb) | [Dataset](./Datasets/Attacks/Paraphrasing%20attack/RT%20paraphrasing/paraphrased_data_fr.csv) |
|6. Run the Detection Algorithm on the [Paraphrased Dataset](./Datasets/Attacks/Paraphrasing%20attack/paraphased-text.csv) | [Part1](./Notebooks/Attacks/Paraphrasing%20Attack/RT%20paraphrasing/Detection/rt-detection-part-1.ipynb) <br> [Part2](./Notebooks/Attacks/Paraphrasing%20Attack/RT%20paraphrasing/Detection/rt-detection-part-2.ipynb) <br> [Part3](.) <br> [Merge](./Notebooks/Attacks/Paraphrasing%20Attack/RT%20paraphrasing/Detection/merge-detection-rt-paraphrased.ipynb)| [Part1](./Datasets/Attacks/Paraphrasing%20attack/RT%20paraphrasing/Detection/paraphrasing_test_results_part1.csv) <br> [Part2](./Datasets/Attacks/Paraphrasing%20attack/RT%20paraphrasing/Detection/paraphrasing_test_results_part2.csv) <br> [Part3](./Datasets/Attacks/Paraphrasing%20attack/RT%20paraphrasing/Detection/paraphrasing_test_results_part3.csv) <br> [Merged](./Datasets/Attacks/Paraphrasing%20attack/RT%20paraphrasing/Detection/detection_merged_data.csv) |
|7. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm after RT Paraphrasing| [Notebook](./Notebooks/Attacks/Paraphrasing%20Attack/RT%20paraphrasing/Detection/evaluate-model-after-rt-paraphrasing.ipynb) | N/A |

### **2. Homoglyph Attack**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Simulate Homoglyph Attack on the [Watermarked Dataset](./Datasets/No%20Attacks/Merged/truncated-watermarked-and-unwatermarked-text.csv)| [Notebook](./Notebooks/Attacks/Homoglyph%20Attack/homoglyph-attack-v1-2.ipynb) | [Dataset](./Datasets/Attacks/Homoglyph%20Attack/homoglyph_data_v2.csv) |
| 2. Run the Detection Algorithm on the [Homoglyph Text](./Datasets/Attacks/Homoglyph%20Attack/homoglyph_data.csv) | [Part1](./Notebooks/Attacks/Homoglyph%20Attack/Detection/detection-homoglyph-part1.ipynb) <br> [Part2](./Notebooks/Attacks/Homoglyph%20Attack/Detection/detection-homoglyph-part2.ipynb) <br> [Part3](./Notebooks/Attacks/Homoglyph%20Attack/Detection/detection-homoglyph-part3.ipynb) <br> [Merge](./Notebooks/Attacks/Homoglyph%20Attack/Detection/merge-homoglyph-detection.ipynb)| [Part1](./Datasets/Attacks/Homoglyph%20Attack/Detection/homoglyph_test_results_part1.csv) <br> [Part2](./Datasets/Attacks/Homoglyph%20Attack/Detection/homogylph_test_results_part2.csv) <br> [Part3](./Datasets/Attacks/Homoglyph%20Attack/Detection/homoglyph_test_results_part3.csv) <br> [Merged](./Datasets/Attacks/Homoglyph%20Attack/Detection/merged_homoglyph_datasets.csv) |
| 3. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm after applying Homoglyph Attack| [Notebook](./Notebooks/Attacks/Homoglyph%20Attack/Detection/evaluate-homoglyph.ipynb) | N/A |
| 4. Counteract the Homoglyph Attack | [Notebook](./Notebooks/Attacks/Homoglyph%20Attack/homoglyph-attack-and-counteracting-v2.ipynb) | [Dataset](./Datasets/Attacks/Homoglyph%20Attack/normalized_data.csv)|

### **3. Zero-Width Attack**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Simulate Zero-width attack on watermarked text | [Notebook](./Notebooks/Attacks/Zero%20Width%20Attack/Simulate%20Attack/zero-width-attack.ipynb)| [Dataset](./Datasets/Attacks/Zero%20Width%20attack/Simulate%20Attack/zero-width-attacked-text.csv)|
| 2. Run the Detection Algorithm on the first 100 samples from the [Zero-width Attacked Dataset](./Datasets/Attacks/Zero%20Width%20Attack/Simulate%20Attack/zero-width-attacked-text.csv)| [Part 1](./Notebooks/Attacks/Zero%20Width%20Attack/Detection/create-pvalue-scores-dataset-zero-width-part-1.ipynb) <br> [Part 2](./Notebooks/Attacks/Zero%20Width%20Attack/Detection/create-pvalue-scores-dataset-zero-width-part-2.ipynb) <br> [Part 3](./Notebooks/Attacks/Zero%20Width%20Attack/Detection/create-pvalue-scores-dataset-zero-width-part-3.ipynb) <br> [Merge](./Notebooks/Attacks/Zero%20Width%20Attack/Merge%20Datasets/create-merged-pvalue-scores-zero-width-dataset.ipynb) | [Part 1](./Datasets/Attacks/Zero%20Width%20attack/Detection/p-value-label-part-1.csv) <br> [Part 2](./Datasets/Attacks/Zero%20Width%20attack/Detection/p-value-label-part-2.csv) <br> [Part 3](./Datasets/Attacks/Zero%20Width%20attack/Detection/p-value-label-part-3.csv) <br> [Merged](./Datasets/Attacks/Zero%20Width%20attack/Merge%20Datasets/p-values%20zero-width%20attack.csv) |
| 3. Evaluate the Accuracy, Precision, Recall and F1-score  of the Detection Algorithm after Zero-Width Attack **without** counteracting | [Notebook](./Notebooks/Attacks/Zero%20Width%20Attack/Detection/evaluate-the-detection-algorithm-zero-width-no-counteracting.ipynb) | N/A |
| 4. Counteract the Zero-Width Attack | [Notebook](./Notebooks/Attacks/Zero%20Width%20Attack/Counteract%20Attack/counteract-zwc-v2-0.ipynb) | [Dataset](./Datasets/Attacks/Zero%20Width%20attack/Counteract%20Attack/recovered_ZW_data-v2.csv) |

### **4. Bidirectional Reordering Attack**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Simulate Bidirectional Reordering attack on watermarked text | [Notebook](./Notebooks/Attacks/Bidirectional%20Reordering%20Attack/bidi-attack.ipynb)| [Dataset](./Datasets/Attacks/Bidirectional%20Reordering%20Attack/bidi_reordered_attacked.csv)|
| 2. Run the Detection Algorithm on the first fews samples from the [Bidirectional Reordering Attack Dataset](./Datasets/Attacks/Bidirectional%20Reordering%20Attack/bidi_reordered_attacked.csv)| [Part 1](./Notebooks/Attacks/Bidirectional%20Reordering%20Attack/detection-opt-350m-reordering-taher.ipynb)| [Part 1](./Datasets/Attacks/Bidirectional%20Reordering%20Attack/permutation_test_results_bidi.csv)|
| 3. ***FAILED*** Use OCR as a method for reversing Reordering Attack | [Notebook](./Notebooks/Attacks/Bidirectional%20Reordering%20Attack/bidi-counteract-fail-v1.ipynb)| N/A |
| 4. Use RTL languages detector to evaluate if Bidi characters are unnecessary| [Notebook](./Notebooks/Attacks/Bidirectional%20Reordering%20Attack/bidi-counteract-detect-rtl-v1.ipynb) | [Dataset](./Datasets/Attacks/Bidirectional%20Reordering%20Attack/bidi_analysis_results.csv)|
---

 *Note*: Reordering counteracting using OCR likely failed due to the length of the input, as multiline was not supported. Proposed solution is to detect Right-To-Left (RTL) languages and then evaluate the text for bidi reordering characters. If text is in a Left-To-Right (LTR) language and uses Bidi characters then it's flagged as manipulated.

### **5. Spelling Mistakes Attack (Discrete Alterations)**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Simulate Spelling Mistakes Attack on watermarked text| [Notebook](./Notebooks/Attacks/Spelling%20Mistakes%20Attack/spelling-mistakes.ipynb) | [Dataset](./Datasets/Attacks/Spelling%20Mistakes%20Attack/mispelled_text.csv)|
|2. Used a spellcheck pretrained model on the [Mispelled dataset](./Datasets/Attacks/Spelling%20Mistakes%20Attack/mispelled_text.csv) | [Notebook](./Notebooks/Attacks/Spelling%20Mistakes%20Attack/spellcheck-v1.ipynb)|
|3. Run detection algorithm on the dataset before and after spellcheck | [Before Spellcheck](./Notebooks/Attacks/Spelling%20Mistakes%20Attack/detection-opt-350m-with-spelling-mistakes-v1.ipynb) <br> [After Spellcheck](./Notebooks/Attacks/Spelling%20Mistakes%20Attack/detection-opt-350m-after-spell-check-v1.ipynb) | N/A |

*Note*: Accuracy before spellcheck was 83% and after spellcheck it was significantly reduced to 54%. This can be due to the method we used to introduce spelling mistakes (They simulated typos such as forgetting a letter or swapping any two letters in a word), or some small hallucinations from the language model used for spellcheck.

### **6. Unnecessary Whitespace Attack (Tokenization Attack)**
| Description | Notebooks | Datasets |
| --- | --- | --- |
| 1. Simulate Unnecessary Whitespace Attack  on watermarked text and Undo it (Disadvantages: Removes all newlines) | [Notebook](./Notebooks/Attacks/Unnecessary%20Whitespace%20Attack/unnecessary-whitespace-v2.ipynb) | [Dataset](./Datasets/Attacks/Unnecessary%20Whitespace%20Attack/modified_and_cleaned_text_v2.csv) |
| 2. Remove unnecessary whitespace from dataset (watermarked and unwatermarked) | [Notebook](./Notebooks/Attacks/Unnecessary%20Whitespace%20Attack/remove-unnecessary-whitespace.ipynb)| [Dataset](./Datasets/Attacks/Unnecessary%20Whitespace%20Attack/merged_data.csv)|
| 3. Run detection algorithm on the modified [dataset](./Datasets/Attacks/Unnecessary%20Whitespace%20Attack/modified_and_cleaned_text_v2.csv) | [Before](./Notebooks/Attacks/Unnecessary%20Whitespace%20Attack/detection-opt-350m-add-unnecessary-whitespace.ipynb) <br> [After](./Notebooks/Attacks/Unnecessary%20Whitespace%20Attack/detection-opt-350m-remove-unnecessary-white.ipynb) | N/A |

## **Evaluating LLM With and Without Watermark**
| Description | Notebooks | Datasets |
| --- | --- | --- |
|1. Evaluate OPT-350M (No Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [MCQ FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt-350m-mcq-hellaswag-v1.ipynb) <br> [Auto-Complete FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt-350m-autocomplete-hellaswag-v1.ipynb)<br>[Minimum Loss](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-loss-v1.ipynb)<br> [MMLU Notebook Adaptation](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-maxnewtoken1-v2.ipynb) <br> [MMLU Notebook Adaptation Results Analysis](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-maxnewtoken1-v2-analysis-v1.ipynb) <br> [MMLU Adaptation with one example and Analysis](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-maxnewtoken1-v3-one-example-analysis.ipynb) <br> [MMLU one examples F1-Score, Accuracy, Precision, Recall](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-unwatermark-evaluation.ipynb)| [MCQ](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/opt_few_shot_results_mcq.csv) <br> [Auto-Complete](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/opt_few_shot_results_autocomplete.csv) <br> [MMLU Notebook Adaptation Output](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/evaluation_OPT_350mb.csv)<br> [MMLU Notebook Adaptation Metrics Input](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/run_results_OPT_350mb.csv)<br>[MMLU Adaptation with one example](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/evaluation_OPT_350mb-one-example.csv)|
|2. Evaluate OPT-350M (With Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [Part 1](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p1.ipynb) <br> [Part 2](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p2.ipynb) <br> [Part 3](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p3.ipynb) <br> [Part 4](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p4.ipynb) <br> [Part 5](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p5.ipynb) <br> [Part 6](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p6.ipynb) <br> [Part 7](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p7.ipynb) <br> [Part 8](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p8.ipynb) <br> [Part 9](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p9.ipynb) <br> [Part 10](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p10.ipynb) <br> [Part 11](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p11.ipynb) <br> [Part 12](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p12.ipynb) <br> [Part 13](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p13.ipynb) <br> [Part 14](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p14.ipynb) <br> [Part 15](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/HellaSwag/hellaswag-eval-watermarked-p15.ipynb) <br> [Merge and Analysis](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag-eval-analysis-watermarked.ipynb)| [Part 1](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p1.csv) <br> [Part 2](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p2.csv) <br> [Part 3](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p3.csv) <br> [Part 4](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p4.csv) <br> [Part 5](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p5.csv) <br> [Part 6](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p6.csv) <br> [Part 7](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p7.csv) <br> [Part 8](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p8.csv) <br> [Part 9](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p9.csv) <br> [Part 10](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p10.csv) <br> [Part 11](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p11.csv) <br> [Part 12](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p12.csv) <br> [Part 13](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p13.csv) <br> [Part 14](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p14.csv) <br> [Part 15](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/hellaswag_evaluation_OPT_350mb_watermarked_p15.csv) <br> [Merged](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/merged_hellaSwag_evaluation_watermarked.csv)|
|***FAILED & ABANDONED*** Evaluate GEMMA-2B (No Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [MCQ and Auto-Complete FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/gemma-mcq-and-autocomplete-v1-FAIL.ipynb) | N/A |
|3. Evaluate OPT-350M (With Watermark) using the [HellaSwag Dataset](https://www.github.com/rowanz/hellaswag) | [Logits with Red-Green List (Minimum Loss) FAIL](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/opt350m-evaluating-a-watermark-for-llm-fail-v1.ipynb)| N/A |
| 4. Evaluate OPT-350M (Without watermark) using the [MMLU Dataset](https://github.com/hendrycks/test)| [MCQ Eval for all categories](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu-opt-350m-eval-without-watermark-v2.ipynb)<br> [MMLU Analysis F1-Score, Accuracy, Precision, Recall](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/analysis-mmlu-unwatermarked.ipynb)| N/A |
| 5. Evaluate OPT-350M (With watermark) using the [MMLU Dataset](https://github.com/hendrycks/test)| [Part 1](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p1.ipynb) <br> [Part 2](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p2.ipynb) <br> [Part 3](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p3.ipynb) <br> [Part 4](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p4.ipynb) <br> [Part 5](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p5.ipynb) <br> [Part 6](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p6.ipynb) <br> [Part 7](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p7.ipynb) <br> [Part 8](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p8.ipynb) <br> [Part 9](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p9.ipynb) <br> [Part 10](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p10.ipynb) <br> [Part 11](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p11.ipynb)  <br> [Part 12](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p12.ipynb) <br> [Part 13](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p13.ipynb) <br> [Part 14](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p14.ipynb) <br> [Part 15](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p15.ipynb) <br> [Part 16](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p16.ipynb) <br> [Part 17](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p17.ipynb) <br> [Part 18](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p18.ipynb) <br> [Part 19](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p19.ipynb) <br> [Part 20](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p20.ipynb) <br> [Part 21](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/MMLU/mmlu-opt-350m-eval-with-watermark-p21.ipynb)  <br> [Merge](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu-eval-analysis-watermarked.ipynb) | [Part 1](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p1.json) <br> [Part 2](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p2.json) <br> [Part 3](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p3.json) <br> [Part 4](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p4.json) <br> [Part 5](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p5.json) <br> [Part 6](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p6.json) <br> [Part 7](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p7.json) <br> [Part 8](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p8.json) <br> [Part 9](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p9.json) <br> [Part 10](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p10.json) <br> [Part 11](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p11.json)  <br> [Part 12](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p12.json) <br> [Part 13](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p13.json) <br> [Part 14](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p14.json) <br> [Part 15](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p15.json) <br> [Part 16](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p16.json) <br> [Part 17](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p17.json) <br> [Part 18](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p18.json) <br> [Part 19](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p19.json) <br> [Part 20](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p20.json) <br> [Part 21](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/mmlu_run_results_OPT_350mb_watermarked_p21.json)  <br> [Merged](./Datasets/No%20Attacks/Evaluation/Automated%20Evaluation/merged_MMLU_watermarked_results.json)|
| 6. Evaluate OPT-350M (Without watermark) using the [TruthfulQA Dataset](https://github.com/sylinrl/TruthfulQA)| [Evaluation using ROUGE, BLEU, BLEURT](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/truthfulqa-opt-350m-eval-without-watermark-v2.ipynb)| N/A |
| 7. Evaluate OPT-350M (With watermark) using the [TruthfulQA Dataset](https://github.com/sylinrl/TruthfulQA)| [Evaluation using ROUGE, BLEU, BLEURT](./Notebooks/No%20Attacks/Evaluation/Automated%20Evaluation/truthfulqa-opt-350m-eval-with-watermark-v1.ipynb) | N/A |
