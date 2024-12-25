# [YOLO11](https://github.com/ultralytics/ultralytics)

## 概述
[DOCS](https://docs.ultralytics.com/models/yolo11/)<br>
YOLO11 是 Ultralytics YOLO 系列即時物體偵測器的最新版本，以尖端的精度、速度和效率重新定義了可能性。 YOLO11 在先前 YOLO 版本令人印象深刻的進步的基礎上，在架構和訓練方法上引入了重大改進，使其成為各種電腦視覺任務的多功能選擇。
![](https://raw.githubusercontent.com/ultralytics/assets/refs/heads/main/yolo/performance-comparison.png)

### 主要特點
* **增強的特徵提取:** YOLO11採用改良的主幹和頸部架構，增強了特徵提取能力，以實現更精確的目標偵測和複雜任務表現。
* **針對效率和速度進行最佳化:** YOLO11引入了精緻的架構設計和優化的訓練管道，提供更快的處理速度並保持準確性和性能之間的最佳平衡。
* **使用更少的參數獲得更高的精度：** 隨著模型設計的進步，YOLO11m 在 COCO 資料集上實現了更高的平均精度 (mAP)，同時使用的參數比 YOLOv8m 少 22%，從而在不影響精度的情況下提高計算效率。
* **跨環境的適應性:** YOLO11可無縫部署在各種環境中，包括邊緣設備、雲端平台和支援NVIDIA GPU的系統，確保最大的靈活性。
* **廣泛的支援任務:** 無論是物件偵測、實例分割、影像分類、姿態估計或定向物件偵測 (OBB)，YOLO11 都旨在應對各種電腦視覺挑戰。

### 支援的任務和模式
YOLO11 基於 YOLOv8 中引入的多功能模型系列構建，為各種計算機視覺任務提供增強的支援：
![](https://github.com/rkuo2000/yolo11/blob/main/assets/YOLO11_tasks_and_modes.png?raw=true)

### 效能指標
![](https://github.com/rkuo2000/yolo11/blob/main/assets/YOLO11_performance_metrics.png?raw=true)

### 使用範例
PyTorch 預先訓練的 *.pt 模型以及配置 *.yaml 檔案可以傳遞給 YOLO() 類，以在 Python 中建立模型實例：<br>

```
from ultralytics import YOLO

# Load a COCO-pretrained YOLO11n model
model = YOLO("yolo11n.pt")

# Train the model on the COCO8 example dataset for 100 epochs
results = model.train(data="coco8.yaml", epochs=100, imgsz=640)

# Run inference with the YOLO11n model on the 'bus.jpg' image
results = model("path/to/bus.jpg")
```

### 如何訓練YOLO11模型

```
from ultralytics import YOLO

# Load a COCO-pretrained YOLO11n model
model = YOLO("yolo11n.pt")

# Train the model on the COCO8 example dataset for 100 epochs
results = model.train(data="coco8.yaml", epochs=100, imgsz=640)
```

