# ELEC5622 Project 2: HEp-2 image classification

## Contents

- `ELEC5622_Project2_VSCode.ipynb`: complete experimental source notebook with saved execution outputs (the record of the reported run). Its final section (11) regenerates report Figures 1, 4, 5 and 7 from the saved result CSVs; it was added after the run and has no saved outputs.
- `Requirements.txt`: Python dependencies used by the notebook.
- `report/ELEC5622_Project2_HD_Report.docx`: project report.

Training outputs (checkpoints, CSV metrics, figures) are written to `./ELEC5622_Project2/results/` and are gitignored.

## Data (not included as required)

Obtain the original tutor-provided files and extract the dataset directory in the same folder as the notebook. The notebook expects:

```
./ELEC5622_Project2_VSCode.ipynb
./Requirements.txt
./gt_training.csv
./Three Datasets for Training, Validation and Test/training/*.png
./Three Datasets for Training, Validation and Test/validation/*.png
./Three Datasets for Training, Validation and Test/test/*.png
```

## Environment and execution

Create a Python 3.11 virtual env

```
python -m pip install -r Requirements.txt
```

## Four experiments

- AlexNet, partial fine-tuning: train classifier; freeze convolutional extractor.
- AlexNet, full fine-tuning.
- ResNet34, partial fine-tuning: train `layer4` and `fc`.
- ResNet34, full fine-tuning.

## Evaluation and reported outputs

Training and validation accuracy, test accuracy, macro F1, per-class precision/recall/F1, confusion matrices, trainable parameter counts and training-only elapsed time. The separately submitted experiment-results archive contains CSV metrics and PNG figures.
