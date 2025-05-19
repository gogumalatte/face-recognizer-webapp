# 🧑‍🦲 안면 인식 웹 애플리케이션 (Flask + face_recognition)

이 프로젝트는 **Flask 웹 프레임워크**와 **face_recognition 라이브러리**를 활용하여, 사용자의 웹캠으로 캡처한 얼굴 이미지를 **기존 등록된 얼굴과 비교**하고, **일치 여부를 실시간으로 판단**하는 웹 애플리케이션입니다.  
**WebSocket 통신**을 통해 이미지 데이터를 실시간으로 서버에 전송하고, **결과를 즉시 사용자에게 표시**하는 구조입니다.

---

## 📷 데모 화면

<img width="700" alt="face-match-demo" src="https://github.com/user-attachments/assets/54bf6a30-e0ed-4474-bd53-73178f2b812d" />

---

## 🚀 실행 방법

### 1. 로컬 환경에서 실행
```bash
# 패키지 설치
pip install flask flask-cors flask-sock opencv-python face_recognition pyngrok

# 등록된 얼굴 이미지 준비 (예: known_face.jpg)
# 서버 실행
python app.py

# 웹 브라우저에서 http://localhost:3000 접속
# 웹캠 접근 권한 허용 후 얼굴 캡처 및 인식 결과 확인
```

### 2. 구글 코랩에서 실행
```bash
# Ngrok 토큰 등록
!ngrok authtoken <your_token>

# run_server.py 실행
!python run_server.py

# 출력된 URL을 브라우저에서 열면 외부에서 테스트 가능
```
---

## 💡 핵심 기능
### 📸 웹캠 실시간 영상 스트리밍 (HTML5 + JS)
### ✂️ 캡처된 이미지 WebSocket으로 서버 전송
### 🧠 서버에서 등록된 얼굴과 비교 (face_recognition)
### ✅ 일치 여부를 실시간으로 사용자에게 전달

---
## 🧩 기술 스택
| 영역     | 사용 기술                                          |
| ------ | ---------------------------------------------- |
| 백엔드    | Python, Flask, flask-sock, flask-cors          |
| 얼굴 인식  | face\_recognition, dlib, numpy                 |
| 프론트엔드  | HTML, JavaScript (getUserMedia, WebSocket API) |
| 영상 처리  | OpenCV                                         |
| 테스트 환경 | Google Colab + Ngrok                           |

---
## 📁 디렉토리 구조
```bash
.
├── app.py
├── face_data
│   └── 최기영.json (얼굴 등록한 파일)
├── run_server.py
├── sample_data
│   ├── anscombe.json
│   ├── california_housing_test.csv
│   ├── california_housing_train.csv
│   ├── mnist_test.csv
│   ├── mnist_train_small.csv
│   └── README.md
└── www
    └── index.html
```

---
## 🛠 향후 개선 방향
### 🧾 여러 명의 얼굴 등록 및 식별 기능 추가
### 🔒 API 키 또는 사용자 등록 기능과 연동
### 🎨 UI 개선 (반응형 디자인, 상태 표시)
### 📁 인식 결과 로그 저장 기능

---
## 🧑‍💻 개발자
### 👤 최기영
### 고급 웹 프로그래밍 과제 프로젝트


