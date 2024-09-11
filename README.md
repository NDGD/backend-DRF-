## NDGD
![image](https://github.com/user-attachments/assets/ed9f14a9-6d2c-4351-bf3b-3aa07db40f44)

- 🗓️프로젝트 기간: 2023-06-10 ~ 2023-07-22
- 📌[시연영상](https://drive.google.com/drive/folders/180hnEssX2zDTlv8xGnfC0JiUbH4XvQEU)

## NDGD 소개
🚀인공지능을 이용한 개인 맞춤형 산재보상 정보 제공 서비스입니다.
- 구현배경
  
  - 노동자가 본인의 상황에 따른 가능한 보상 정도에 대해 어느 정도 파악하고 있어야 좋은 노무사또는 변호사를 선택할 수 있지만 노동자가 개인적으로 파악하기엔 어려움이 있습니다. 이를 위해 개인 맞춤형 산재 보상 정보를 제공하는 서비스가 필요하다고 생각하였습니다.
  - 산재 승인 및 보험금 수령의 절차가 복잡하며 관련 , 정보가 분산되어 있기 때문에 산재가 발생했을 때 노동자 스스로 수많은 검색의 단계를 거쳐야 합니다. 이때문에 기존의 웹사이트들 보다 좀 더 직관적이고 실질적인 도움이 되는 정보를 제공하는 웹 플랫폼이 필요하다고 생각하였습니다.  

🌟두 가지 아이디어를 바탕으로 개인 , 맞춤형 산재 보상 정보를 제공할 뿐민 아니라 노동자에게 필요한 정보를 직접 제공 또는, 해당 정보가 있는 곳으로 연결해 주는 플랫폼이 될 웹서비스를 구현하였습니다.

## Install
git clone
```bash
git clone
cd backend-DRF-
```
make venv
```bash
python -m venv ndgd
```
activate venv
- Windows
  ```bash
  .\ndgd\Scripts\activate
  ```
- macOS/Linux
  ```bash
  source ndgd/bin/activate
  ```

modules install
```bash
pip install -r requirements.txt
```

Runserver
```bash
cd api
python manage.py runserver
```
📌[Go to frontend Install](https://github.com/NDGD/front)

## 기술스택
<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">  
<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black"> <img src="https://img.shields.io/badge/django-092E20?style=for-the-badge&logo=django&logoColor=white">  
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white"/>  

- AI모델 임베딩을 위하여 Django 채택

## 개발 포인트
- 공공데이터 활용
  
  - 공공데이터 포탈의 근로복지공단 data를 활용하여 AI 학습
  - 한국어에 특화된 자연어 처리 모델 KoBert와 사전에 학습시킨 K-means 모델을 이용해 수령 가능한 보험금을 예측
- 용이한 유지보수
  
  - 근로복지공단에서 2018년 부터 매년 제공하는 공공데이터이기 때문에 확보의 지속성이 어느정도 보장
  - 1년 단위로 최신 데이터를 제공받아 기존의 AI 알고리즘을 학습하여 서비스를 제공할 수 있음
