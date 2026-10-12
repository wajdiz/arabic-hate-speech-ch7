# Companion materials: Chapter 7, Hate Speech Detection in Arabic

Companion files for Activities 2 and 3 of Chapter 7, *Hate Speech Detection in Arabic: Concepts, Resources, and Practical Approaches for Digital Humanities*, in the edited volume *Arabic Digital Humanities*.

## Files

| File | For | Contents |
|---|---|---|
| `Chapter7_Activities_2_3.ipynb` | Students and instructors | Colab notebook: loads L-HSAB, draws the prepared sample, computes Cohen's kappa, trains a classifier, compares it with human labels, writes a disagreement sheet |
| `sample_student.csv` | Students | 30 tweets (10 per L-HSAB label), item ID and text only |
| `annotation_template.csv` | Students | Columns: `annotator_A`, `annotator_B`, `adjudicated`, `justification` |
| `sample_key.csv` | Instructor only | L-HSAB reference labels for the 30 items |

The notebook regenerates all three CSV files (random seed 42), so the sample is the same in every run.

## Running the notebook

1. Open `Chapter7_Activities_2_3.ipynb` in Google Colab (File > Upload notebook). No GPU is needed.
2. Run Steps 1 and 2.
3. Annotate `annotation_template.csv` with labels `hate`, `offensive`, or `neither`. Save it as `my_annotations.csv` and upload it to the Colab Files panel.
4. Run the remaining steps. Fill in the `category` column of `disagreements.csv` with one of: `model error`, `human annotation error`, `label-scheme difference`, `guideline ambiguity`.

Requirements: Python 3 with pandas, NumPy, and scikit-learn, all preinstalled in Colab.

## Data

L-HSAB is downloaded at run time from its public repository: https://github.com/Hala-Mulki/L-HSAB-First-Arabic-Levantine-HateSpeech-Dataset

Mulki, H., Haddad, H., Bechikh Ali, C., & Alshabani, H. (2019). L-HSAB: A Levantine Twitter dataset for hate speech and abusive language. In *Proceedings of the Third Workshop on Abusive Language Online* (pp. 111–118). Association for Computational Linguistics. https://doi.org/10.18653/v1/W19-3512

The sample contains offensive and hateful content and is intended for teaching and research only.
