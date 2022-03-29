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
def classified_by_class(list_boxex_info, class_names): | class 별로 box 정보를 모음
def data_distribution(dict_classified_by_class, class_names): | class 별로 data distribution을 측정
def sort_by_score_detection(dict_classified_by_class, class_names): | score 순으로 정렬
def iou(b1, b2): | iou를 계산
def cal_ap(detection, groundtruth, class_names): | class 별로 recall, precision 을 Threshohold에 따라 계산
def make_plot(result_cal_ap, class_name): | AP 그래프를 recall, precision 에 따라 시각화
def cal_area(result_cal_ap, class_name): | AP 그래프의 넓이 계산

test
