# Fluorescent penetrant inspection (FPI, DP, LPI, PT)
Detection of liquid penetrant test with AI (Yolo11)

### MODEL
- Yolo11l: https://huggingface.co/jparedesDS/liquid-penetrant-test-detection

#### Supported Labels
['defecto']

#### ALL my models YOLOv10 & YOLOv9
- Yolov9c: https://huggingface.co/jparedesDS/cs2-yolov9c
- Yolov10s: https://huggingface.co/jparedesDS/cs2-yolov10s
- Yolov10m: https://huggingface.co/jparedesDS/cs2-yolov10m
- Yolov10b: https://huggingface.co/jparedesDS/cs2-yolov10b
- Yolov10b: https://huggingface.co/jparedesDS/valorant-yolov10b
- Yolo11x: https://huggingface.co/jparedesDS/welding-defects-detection

#### How to use
```
from ultralytics import YOLO

# Load a pretrained YOLO model
model = YOLO(r'weights\yolo11l_LPI.pt')

# Run inference on 'image.png' with arguments
model.predict(
    'image.png',
    save=True,
    device=0
    )
```
#### Confusion matrix normalized
![confusion_matrix_normalized.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/cW-e-XzOwhyTbaNdCHEJc.png)
#### Labels
![labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/eVEQyEO6ddZVgPW9RdzOu.jpeg)
#### Results
![results.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/xgQm7K5mSHq9cDwDLW8Hz.png)
#### Predict
![val_batch1_labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/7n8JsgcalT6nAMgpAdB4V.jpeg)
![val_batch2_labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/81CEGAahhFqSZ7PaW-ai3.jpeg)
```
YOLO11l summary (fused): 464 layers, 25,280,083 parameters, 0 gradients, 86.6 GFLOPs
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100%|██████████| 12/12 [00:05<00:00,  2.32it/s]
                   all        836        752      0.794      0.771      0.793      0.379
```

#### Others models...
https://huggingface.co/jparedesDS/welding-defects-detection
