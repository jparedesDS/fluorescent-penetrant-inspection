# Liquid Penetrant Test (DP, LPI, PT)
Detection of liquid penetrant test with AI (Yolo11)

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
model = YOLO(r'weights\liquid-penetrant-test-detection-yolo11l.pt')

# Run inference on 'image.png' with arguments
model.predict(
    'image.png',
    save=True,
    device=0
    )
```
#### Confusion matrix normalized
![confusion_matrix_normalized.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/tE3CoiaB8ODKdQs_gTWTp.png)
#### Labels
![labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/okW-nqDnryqccYbsDt-ra.jpeg)
#### Results
![results.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/k7lUu5uaNXISLyGfLkOdX.png)
#### Predict
![val_batch2_labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/_ku6Baq6CrSkE7ap4zQbn.jpeg)
![val_batch1_labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/EK7SfvdOdUAY8d20IXzqI.jpeg)
```
YOLO11m summary (fused): 303 layers, 20,031,574 parameters, 0 gradients, 67.7 GFLOPs
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100%|██████████| 11/11 [00:06<00:00,  1.71it/s]
                   all        999       2016      0.963      0.898      0.931      0.655
                  Body        966       1029      0.971      0.935      0.958      0.791
                  Head        936        987      0.955      0.862      0.904      0.519
```

#### Others models...
https://huggingface.co/jparedesDS/welding-defects-detection
