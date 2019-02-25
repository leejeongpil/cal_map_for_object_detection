# cal_map_for_object_detection
Object detection 의 평가지표가 되는 mAP를 구현한 코드입니다.

## How to use
### 1. 아래의 box 형식에 맞춰 .txt 파일을 저장 합니다.

folder | detections | groundtruths
------ | ------ | ------
file name | file_name.txt | file_name.txt
contents | class score xmin ymin xmax ymax | class xmin ymin xmax ymax

### 2. cal_metrics_jp.ipynb 파일을 실행합니다.

## function explain

function_name | role
------ | ------
def extract_detection_info(paths): | detections folder 에서 정보를 뽑음
def extract_groundtruth_info(paths): | groundtruths folder 에서 정보를 뽑음
def classified_by_class(list_boxex_info, class_names): | class 별로 box 정보를 

