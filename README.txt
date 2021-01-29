[For training]
./darknet detector train /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/senriai.data /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/yolov4.cfg yolov4.conv.137 -map

[For Training with log]
./darknet detector train /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/senriai.data /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/yolov4.cfg darknet53.conv.74 -map | grep "avg loss" | tee /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/log.txt

[For video prediction]
./darknet detector demo /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/senriai.data /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/yolov4.cfg /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/backup/yolov4_last.weight test1.mp4

[For evaluation mAP]
./darknet detector map /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/senriai.data /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/yolov4.cfg /home/ic1/darknet/logs/DCON2021_SenriAi/Southeast_Botanical_Gardens/backup/yolov4_last.weight -iou_thresh 0.75
