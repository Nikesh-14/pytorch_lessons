# PyTorch Animal Image Classification

---

## Dataset

[Animal Image Dataset (Kaggle)](https://www.kaggle.com/datasets/aakashhaldankar/animal-image-dataset)

Not included in the repo, download it yourself. Folder structure should look like this:

```
dataset/
    training/
        cat/
        dog/
        ...       ← 40 images per class
    test/
        cat/
        dog/
        ...       ← 10 images per class
```

---

## Setup

```bash
conda create -n dl-workshop python=3.10
conda activate dl-workshop
pip install -r requirements.txt
```

Then open `nikesh_pytorch.ipynb`, find `DATASET_ROOT` in Cell 4 and change the path to wherever you put the dataset:

```python
DATASET_ROOT = Path(r"your\path\here")
```

Run all cells. That's it.

---

## Troubleshooting

- **Path not found** → you probably didn't update `DATASET_ROOT`
- **DataLoader stuck** → set `num_workers=0`
- **Out of memory** → lower `BATCH_SIZE` to 8
- **Plot not showing** → add `%matplotlib inline` at the top of the notebook

---

## Requirements

```
torch, torchvision, Pillow, numpy, matplotlib, ipykernel
```
