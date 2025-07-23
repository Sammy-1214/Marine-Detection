# 🐠 Marine Species Detection using YOLOv5

This project showcases a deep learning-based solution to identify and classify **marine species** like fish, jellyfish, and sharks from underwater images. Leveraging the power of **YOLOv5**, a state-of-the-art object detection model, it aims to assist marine research, biodiversity monitoring, and conservation efforts through automation.

## 🌊 Project Motivation

Manual identification of underwater species can be time-consuming and error-prone. This project automates the detection process using computer vision, enabling faster, scalable, and more accurate marine species monitoring.

##

## 📁 Dataset Overview

The dataset used is a custom-labeled set of underwater images with annotations for:
- **Fish**
- **Jellyfish**
- **Sharks**  
- And other marine life (expandable via `data.yaml`)

The dataset is split into:
- `train/` – Training images with labels  
- `valid/` – Validation set for performance evaluation  
- `test/` – Final testing and inference

YOLO-ready annotations are in `.txt` format with class and bounding box details.


##


## 🧠 Model & Training Details

- Model Used: `YOLOv5m` (medium variant for balance between accuracy and speed)
- Framework: **PyTorch**
- Input Size: `640x64`
- Epochs: `100`
- Batch Size: `16`
- Training Command:

##


### 📈 Evaluation Metrics

| **Metric**       | **Score** |
|------------------|-----------|
| **Precision**    | 0.92      |
| **Recall**       | 0.87      |
| **F1 Score**     | 0.89      |
| **mAP@0.5**      | 0.91      |
| **mAP@0.5:0.95** | 0.84      |

📌 *Training and validation metric plots (loss, precision, recall, mAP) are available in:*  
`runs/train/marine_yolo5m_final/`



##


🔍 Inference Example
To detect marine species in new images, run:

python detect.py --weights runs/train/marine_yolo5m_final/weights/best.pt \
                 --source aquarium_pretrain/test/images \
                 --conf 0.25 \
                 --save-txt \
                 --save-conf \
                 --name marine_test
📁 Predicted images and detection labels will be saved in:
runs/detect/marine_test/



##


👩‍💻 Author
**Hritika Gore**

🎓 Engineering student | 💻 Python & AI Enthusiast | 🧠 Passionate about Machine Learning


##

**💡 Future Improvements**
Expand to more marine species classes

Integrate real-time detection via webcam or underwater drones

Deploy the model using Streamlit or Flask for user interaction




##

🌊 Empowering ocean conservation with the power of deep learning.
```bash
