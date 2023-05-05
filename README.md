# 😷🩺 [DL]skin_disease 🩺🩹
프로젝트 기간 : 2023.4.7 - 2023.4.26
</br>

## 1️⃣ 프로젝트 주제

이미지 기반 피부 종양 분류 작업

</br>

## 2️⃣ 주제 선정 이유
- 코로나19이후 여러 원격 진료 분야가 생겨나고 있으며 그 중 텔레더마톨로지(원격피부질환진료)가 의학계에서 주목
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
- 5번(멜라닌 세포모반)에 해당하는 병변 수는 7970장으로, 가장 많은 것으로 나타남

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

<img width="326" alt="image" src="https://user-images.githubusercontent.com/122995812/236398587-f7be1dc8-edda-476f-8881-9f7c52467af5.png">
> [EfficientNetB5]

Test_acc : 0.86 </br>
Val_acc : 0.79 </br>
Test_acc : 0.72 </br>

</br>

## 8️⃣ 검증
<img width="505" alt="image" src="https://user-images.githubusercontent.com/122995812/236396785-3aec873b-b029-4f37-bac0-71634c0d17c3.png">
- Test_data로 검증
- 사진과 일치하는 병변으로 예측

</br>

## 9️⃣ 기대 효과
- 원격진료 정확도 상승
- 피부 질환 비대면으로 자가진단 가능

</br>

---
</br>

## 🤔 회고
주제가 이미지 분류이기 때문에 데이터 전처리와 EDA과정에서 한계가 있어서 다소 아쉬웠음 </br>
데이터 증강 과정을 거쳤는데, 증강 후 모델의 성능이 감소하여 원인 찾아봄 </br>
-> 병변 데이터는 Random 증강 조심! (병변이 사라질 수도 있음) </br>
-> 증강 시, 같은 클래스에 속하는 서로 다른 데이터의 부분을 교차하는 이미지 증강을 시도하였으나, 코드  오류로 실행하지 못하였음 </br>

