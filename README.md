# SmartFactory2_Assignment

# 소스 코드들을 Zip파일로 다운받아주십시오.
1. 압축을 해제하신 후, 생성되는 ‘Smartfactory_Stacking Ensemble’ 파일을 쥬피터 노트북의 워킹 디렉토리로 이동시켜 주십시오. (윈도우의 경우, 기본으로 설정되는 워킹 디렉토리 : C:\Users\(사용자명)입니다)
또는 ‘Smartfactory_Stacking Ensemble’ 내에 존재하는 모든 파일과 폴더를 쥬피터 노트북에 직접 업로드해주세요. (실행을 위해서는 어떤 파일과 폴더도 빠뜨리지 않는 것이 중요합니다)
2. ‘run_code’ 내의 소스 코드를 다음과 같은 순서로 실행해주십시오
1) data_preprocessing.ipynb  (기본적인 전처리 및 Manual Feature Extraction 수행 코드)
   : 코드 실행에 약 30분 가량 소모되며, 실행 결과로 ‘data’ 폴더 내에 ‘X_MFE.pickle’ , ‘y.pickle’, ‘X_CNN_64.pickle’ 파일이 생성됩니다.
   : 만약 본 코드 실행을 생략하고 싶으시다면 ‘data’ 폴더 내의 ‘결과1’ 폴더 내에 존재하는 파일 3개를 ‘data’ 폴더 내로 옮겨주십시오.
2) run_CNN.ipynb (CNN 모델 학습 및 CNN 모델을 이용한 예측 수행 코드)
   : 코드 실행에 약 3일 가량 소모되며, 실행 결과로 ‘result’ 폴더 내에 총 8개의 pickle 파일이 생성됩니다. (파일명: WMPC_CNN_(숫자)_0_f1_score.pickle 또는 WMPC_CNN_(숫자)_0_softmax.pickle)
   : 코드 실행에 매우 장시간이 소모되므로 코드 실행 생략을 추천드립니다. 만약 본 코드 실행을 생략하고 싶으시다면 ‘result’ 폴더 내의 ‘결과2’ 폴더 내에 존재하는 파일 8개를 ‘result’ 폴더 내로 옮겨주십시오.
3) run_MFE.ipynb (앞서 추출한 특징을 기반으로 FNN 모델 학습 및 예측 수행 코드)
   : 코드 실행에 약 30분 가량 소모되며, 실행 결과로 ‘result’ 폴더 내에 총 8개의 pickle 파일이 생성됩니다. (파일명: WMPC_MFE_(숫자)_0_f1_score.pickle 또는 WMPC_MFE_(숫자)_0_softmax.pickle)
   : 만약 본 코드 실행을 생략하고 싶으시다면 ‘result’ 폴더 내의 ‘결과3’ 폴더 내에 존재하는 파일 8개를 ‘result’ 폴더 내로 옮겨주십시오.
4) run_Stacking.ipynb (Stacking Ensemble 모델 학습 및 예측 수행 코드)
   : 코드 실행에 약 30분 가량 소모되며, 실행 결과로 ‘result’ 폴더 내에 총 8개의 pickle 파일이 생성됩니다. (파일명: WMPC_Stacking_(숫자)_0_f1_score.pickle 또는 WMPC_Stacking_(숫자)_0_softmax.pickle)
   : 만약 본 코드 실행을 생략하고 싶으시다면 ‘result’ 폴더 내의 ‘결과4’ 폴더 내에 존재하는 파일 8개를 ‘result’ 폴더 내로 옮겨주십시오.
5) Visualization_Result.ipynb
(MFE-FNN, CNN, Stacking Ensemble 3개의 모델의 예측 결과를 시각화하여 비교하는 코드)
   : 코드 실행에 약 5분 가량 소모되며, 실행을 통해 3개 모델의 학습수에 따른 성능 비교 결과, 각 모델의 Confusion Matrix를 확인할 수 있습니다.
