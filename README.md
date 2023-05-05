# 😷🩺 [DL]skin_disease 🩺🩹
프로젝트 기간 : 2023.4.7 - 2023.4.26

</br>

## 1️⃣ 프로젝트 주제


</br>

## 2️⃣ 주제 선정 이유
- 코로나19이후 여러 원격 진료 분야가 생겨나고 있으며 그 중 텔레더마톨로지(원격피부질환진료)가 의학계에서 주목\
- 목표 : 본인의 피부 상태 사진으로 학습된 모델을 사용하여 질환 자가진단 가능

</br>

## 3️⃣ 데이터
- kaggle data (5GB/ 27,153장)
- Class : 10
- https://www.kaggle.com/datasets/ismailpromus/skin-diseases-image-dataset
- ![image](https://user-images.githubusercontent.com/122995812/236394051-2eddc46a-8093-4774-87a8-db1f91bc5d40.png)

</br>

## 4️⃣ EDA
<img width="470" alt="image" src="https://user-images.githubusercontent.com/122995812/236394244-a0415a56-7959-4c07-b3a7-814c8ed7b8a6.png">
- 5번 병변 수가 7970장으로 가장 많음

</br>

## 5️⃣ Model
<img width="544" alt="스크린샷 2023-05-05 160138" src="https://user-images.githubusercontent.com/122995812/236396413-4c0886cb-481f-47d0-9827-8ac87935eab3.png">



</br>

## 6️⃣ 성능 개선
- Data Augmentation
<img width="283" alt="image" src="https://user-images.githubusercontent.com/122995812/236395757-d981092e-6813-4d75-a317-b993c74161a4.png">
- 증강 후, 전체적으로 수치가 낮아짐 
-> 의료 데이터 특성상, 증강 과정에서 특정 병변이 사라지거나 작아진 걸로 추정

- 정상 데이터 200장 수집
- Fine Tunning


</br>

## 7️⃣ 결과

<img width="365" alt="image" src="https://user-images.githubusercontent.com/122995812/236396646-7e10c1b1-3f08-4686-a92d-b7c49c2305c3.png">
# [EfficientNetB5]

Test_acc : 0.86
Val_acc : 0.79
Test_acc : 0.72

</br>

## 8️⃣ 검증
<img width="505" alt="image" src="https://user-images.githubusercontent.com/122995812/236396785-3aec873b-b029-4f37-bac0-71634c0d17c3.png">
- Test_data로 검증
- 사진과 일치하는 병변으로 예측

</br>


## 9️⃣ 기대 효과
- 원격진료 정확도 상승
- 피부 질환 비대면으로 자가진단 가능
- 
</br>

---
</br>

## 🤔 회고
