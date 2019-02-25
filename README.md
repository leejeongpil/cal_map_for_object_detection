# cal_map_for_object_detection
Object detection 의 평가지표가 되는 mAP를 구현한 코드입니다.

## How to use
### detections folder
1. detections folder에 detection한 결과가 .txt 형태로 들어갑니다.
   file_name.txt
   class score xmin ymin xmax ymax
detections | groundtruth
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
