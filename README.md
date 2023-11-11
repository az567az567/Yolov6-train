# Yolov6-train

The method to install Yolov6
------
cd C:\yolov6  

conda create -n yolov6 python=3.9  

conda activate yolov6  

pip install -r requirements.txt  

Train the model
------
conda activate yolov6  
cd C:\YOLOv6  

python “C:/YOLOv6/tools/train.py” --epochs 5 --workers 4 --batch-size 4 --conf "C:/YOLOv6/configs/yolov6n_finetune.py” --data "C:/YOLOv6/data/dataset.yaml"  

Test the model
------
conda activate yolov6  
cd C:\yolov6  

python "C:/yolov6/tools/infer.py” --weights “C:/YOLOv6/runs/train/exp/6n/weights/best_ckpt.pt” --source “C:/yolov7/yolov7dataset/test/images/1.jpg”  

python "C:/YOLOv6/tools/infer.py” --weights “C:/YOLOv6/yolov6s.pt” --source "rtsp://adminn:098765@192.168.43.50:554/stream1" --device 0  

