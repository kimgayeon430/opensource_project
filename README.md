# 2024 Opensource Programming Final Project
밤양갱갱갱 - 보이스피싱 탐지 프로그램 개발
# 👪 Teammates
[팀장] 210723 김가연 - 데이터 전처리 작업 수행, 딥러닝 모델 구축 및 모델 사용자화 <br>
2215903 권미성 - 데이터 수집, 전처리 및 웹크롤링 <br>
2214940 김민서 - 테스트 용 음성 데이터 예시, 오픈소스 코드 및 api 수집 및 오류 디버깅
# 💡 Prototype
검사받고 싶은 통화 녹음본 및 문자 텍스트 파일을 구글 드라이브에 업로드 한 후 코랩에서 보이스피싱 탐지 모델을 실행시키면 해당 통화, 문자가 보이스피싱일 위험도을 사용자에게 문자로 전송한다. 

![image](https://github.com/kimgayeon430/opensource_project/assets/150680082/55d322a1-8c19-4b0e-b19a-2e07a5caaf85)

# 🚂 Pipeline
## 1. Data Crawling & Collecting
금융감독원 그놈목소리 보이스피싱 음성데이터를 Web Crawling하여 가져온 후, 구글 드라이브에 업로드하여 딥러닝을 위한 데이터 수집
## 2. Data Preprocessing
음성 파일을 텍스트로 변환하기 위한 여러 과정을 거친 후, 변환된 텍스트를 딥러닝을 위해 가공
## 3. Make DeepLearning Model
전처리 과정을 거친 텍스트 파일을 사용해 딥러닝 모델을 구축
## 4. Voicephishing Detection
사용자가 업로드한 음성 파일을 CLOVA Speech Recognition(STT모델)을 사용해 텍스트로 변환<br>
변환된 텍스트를 탐지 모델에 넣어 보이스피싱 위험도를 도출
## 5. Send Detection Result to User
도출된 위험도를 사용자에게 문자로 전송
