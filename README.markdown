# Animal Detection Using Faster R-CNN

A deep learning project using Faster R-CNN with ResNet-50 to detect 10 animal classes (e.g., Bird, Cat, Deer). Trained on Open Images V7, it achieves 74.19% mAP and 99.79% recall. Includes code, documentation, and bounding box visualization.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/animal-detection-project.git
   cd animal-detection-project
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Dataset Setup

1. Download the Open Images V7 dataset using the link in `link_to_Dataset.txt`.
2. Organize the dataset as follows:
   ```
   Dataset/
   ├── train/
   │   ├── Bird/
   │   ├── Cat/
   │   └── ... (other classes)
   ├── validation/
   ├── test/
   ├── normalized_train.csv
   ├── normalized_validation.csv
   └── normalized_test.csv
   ```
   - CSV files should have columns: `image_name`, `label`, `Xmin`, `Ymin`, `Xmax`, `Ymax`, `height`, `width`.
   - Place images in subfolders named after classes (e.g., `Bird`, `Cat`).

## Usage

1. Open `Animal_Object_Detection_FasterRCNN.ipynb` in Jupyter Notebook.
2. Update dataset paths in the notebook (e.g., `/path/to/Dataset/train`).
3. Run the notebook to:
   - Preprocess data
   - Train the Faster R-CNN model
   - Evaluate (mAP, precision, recall)
   - Visualize bounding boxes

## Files

- `Animal_Object_Detection_FasterRCNN.ipynb`: Main code for data preprocessing, training, and evaluation.
- `dl_project_report.docx`: Detailed project report.
- `project_presentation.pptx`: Project presentation slides.
- `link_to_Dataset.txt`: Link to Open Images V7 dataset.
- `requirements.txt`: Required Python libraries.

## Requirements

- Python 3.11+
- GPU (recommended for training)
- See `requirements.txt` for library versions.

## Notes

- Files are currently in the root directory. A folder structure may be added later.
- The model was fine-tuned on a pre-trained Faster R-CNN using PyTorch on Google Colab with a T4 GPU.
- Ensure dataset paths in the notebook match your local setup.