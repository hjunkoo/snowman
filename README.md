# 🖥️ PM 2.5 Measurement


<br>

## Introduction to the Project

- Making a GRADIO that compares and answers the concentration of fine dust indoors and outdoors.
- Discord notification occurs when indoor fine dust is above the threshold.
- Link Discord and mobile phone application to check the notification immediately.
  
<br>

## team member

<div align="center">

| **Kwon Do-hyeon** | **Koo Hyeon-jun** | **Lee soo-hyeon** | **Ryu tae-an** |
| :------: |  :------: | :------: | :------: |
| <img src="https://github.com/user-attachments/assets/f7665068-667d-4409-bf56-ea39f9b2bf10" height=200 width=130>| <img src="https://github.com/user-attachments/assets/115d6c7c-4e78-4057-8436-fb73508a2dc8" height=200 width=150>| <img src="https://github.com/user-attachments/assets/c40d7b0d-f7b1-4572-bada-710346446bdb" height=220 width=160>| <img src="https://github.com/user-attachments/assets/5ca8c56b-651b-4b1a-9b5a-8d73342d7592" height=200 width=150>|

</div>


<br>



## 1. Team Role 

### 🍊Kwon Do-hyeon
- **role**
    - Full Code Implementation
    - Create Discord Notification Bot
    - Create Github

<br>

### 👻Koo Hyeon-jun
- **role**
    - Presentation
    - Implementing OpenAPI Code
<br>

### 😎Lee soo-hyeon
- **role**
    - Full Code Implementation
    - Create Discord Notification Bot
    - Create Github

<br>

### 🐬Ryu tae-an
- **role**
    - Production of PPT
    - Implementing OpenAPI Code
    
<br>

## 2. Project Duration and Measurement Location

### Project Duration

- Full Project Period : 2024-12-01 ~ 2025-12-19

<br>

### Measurement Location

- Student Council of Environmental Engineering Department, Department 515 of Chungnam National University Engineering School

<img src="https://github.com/user-attachments/assets/b3fc8b72-4173-422e-8501-d53862660097" height=400 width=400>



<br>

## 3. Application Technology Overview

### function calling

- **Gradio 및 Arduino**
    - Gradio: It provided an interface to compare outdoor fine dust data with indoor fine dust data collected through Arduino.
- **OpenAPI**
    - OpenAPI Standard: When importing outdoor fine dust data through Air Korea API, OpenAPI specification is used to implement API structure and operation method.
      
### discord

- **Linked to Discord**
   - When the indoor fine dust value exceeds the set threshold, the chatbot is implemented to automatically send a notification using the Discord API.
- **notification message**
   - The notification includes the message "Ventilation is required" along with the indoor fine dust value, and the outdoor fine dust value is also provided to help users determine whether ventilation is possible.

<br>

## 4. Project Details

## (1) Application Technologies and Utilization Methods

### [Measuring instruments and data collection]

  - **Indoor fine dust measurement**
        - A Grove sensor was connected to Arduino to measure indoor fine dust conditions in real time.
        - The data collected through the sensor was linked to the Discord notification system to inform the user of the need for ventilation.
  - **Outdoor fine dust data collection** 
        - We used the Air Korea API to bring the concentration of fine dust outdoors.
        - Based on OpenAPI specifications, function calling was implemented to efficiently request data and structure response data.
        - We compared and analyzed indoor and outdoor data to support better decision making.

### [Chatbot and notification system]
- **Gradio**
    - Using Gradio, we have established a user interface (UI) that can respond to indoor and outdoor fine dust data.

- **Linked to Discord**
    - Using the Discord API, we implemented a system that automatically sends a notification to the user that "ventilation is required" when the indoor fine dust value exceeds a certain threshold.

### [function calling]
- **Automation and Efficiency**
    - The function calling technique was applied to automate the task of requesting and processing data.
    - It supports the integrated analysis of Arduino Grove sensor data and Air Korea API data, providing useful information to users in real time.

<br>

## (2) Detailed characteristics of Grove devices and how to connect them

- **Grove sensor system**
    - **Modular design**: Grove sensors support plug-and-play to make it easy to connect with Arduino.
    - **Measure fine dust**: Accurately measure indoor air quality data based on particle sizes such as PM2.5 and PM10.

- **How to connect the Grove sensor**
    - As shown in the image below, we collected the data by connecting Grove sensor with Arduino UNO.
    
| frising circuit diagram |
|----------|
|<img src="https://github.com/user-attachments/assets/de3fe5e8-9d60-409f-9d32-eb0ca83c07f3" height=500 width=800>|

  - **Pin connection**
    
      - Red (VCC): 5V pin
    
      - Black (GND): GND pin
        
      - Yellow (DATA): D8 pin


---

- **Using in this project**
    - The data collected through the sensor is analyzed in real time, and the Discord notification system informed the user of the need for ventilation.
    - It has been implemented to intuitively respond to and compare indoor and outdoor fine dust data through the Gradio UI.


<br>

## (3) Features and Utilization of Air Korea OpenAPI

- **AirKorea OpenAPI features**
    - Public Data Delivery: Air Korea OpenAPI is a public data platform that provides real-time domestic outdoor air quality information.
    - Various air quality items: You can check the concentration of various air pollutants such as fine dust (PM10), ultrafine dust (PM2.5), ozone (O3), nitrogen dioxide (NO2).
    - Provide regional data: Get real-time air quality information for a specific area (city, county, district) via API calls.

- **Using in the project**
    - Collecting data for Daejeon area PM2.5
    - Using Air Korea OpenAPI, the concentration of ultrafine dust (PM2.5) in the Daejeon area was brought in real time.
    - The outdoor PM2.5 value received through API and the indoor PM2.5 value collected through the Grove sensor were compared and analyzed.

- **How to collect data**
    - Function Calling
    - Based on OpenAPI's request and response structure, function calling techniques were applied to efficiently import data.
    - When requested, the Daejeon area code is delivered as a parameter to query the PM2.5 value of the area.
    - Utilize data
    - The collected outdoor PM2.5 values were analyzed together with the indoor values and expressed visually through the Gradio UI.
    - In connection with the Discord notification system, if the indoor fine dust value exceeds the standard value, the outdoor fine dust condition is provided together to help users determine whether ventilation is necessary.

### Google Colab Code
The code comparing and analyzing Air Korea OpenAPI and indoor data can be found in the link below.
👉 [Google Colab 코드 보기](project_CODE%20(1).ipynb)


---

- **Result**
  
| indoor > outdoor | indoor < outdoor |
| :------: |  :------: |
| <img src="https://github.com/user-attachments/assets/7ba517c3-1148-4664-aab4-419e50870377" height=300 width=300>| <img src="https://github.com/user-attachments/assets/0f6893db-afef-4eb1-8666-1765c4b11563" height=300 width=300>|


<br>

## (4) 디스코드 챗봇 알림 시스템의 세부 내용

- **디스코드 챗봇 생성**
    - **봇 생성**: Discord Developer Portal에서 프로젝트용 챗봇을 생성하였습니다.
    - **토큰 발급**: 챗봇과 서버 간의 통신을 위해 봇 토큰을 발급받고, 이를 코드에 적용하였습니다.
    - **봇 아이디 설정**: 생성된 챗봇을 디스코드 서버에 초대하고, 해당 봇 아이디를 설정하여 프로젝트에 연동했습니다.

- **알림 시스템 구현**
   - **임계값 설정**
        - 임계값은 측정 장소의 특성을 고려하여 평균적인 값을 경험적으로 분석한 뒤, 실험을 통해 임의로 설정하였습니다.
        - 기준값을 초과할 경우 알림이 울리며, 정상 범위 내에 있을 경우 정상 메시지를 보내도록 구현하였습니다.
  
    - **임계값 초과 시 알림**
        - Grove 센서를 통해 측정된 실내 PM2.5 값이 설정된 임계값을 초과하면, 알림이 자동으로 디스코드 서버에 전송됩니다.
        - 메시지에는 실내 PM2.5 값과 실외 PM2.5 값(에어코리아 API 데이터)이 함께 포함되며, 사용자가 환기 여부를 쉽게 판단할 수 있도록 구현하였습니다.

     
    - **디스코드 서버 연동**
        - Python의 `discord.py` 라이브러리를 사용해 챗봇을 서버에 연결하고, 실시간 메시지 전송 기능을 구현하였습니다.
        - 설정된 서버 채널에 실내 공기질 상태와 환기 필요 메시지가 출력됩니다.

    - **핸드폰 알림 연동**
        - 디스코드 모바일 앱을 통해 사용자 핸드폰에도 실시간 알림이 전달됩니다.
        - 이로써 사용자들은 실내 미세먼지 상태를 언제 어디서나 빠르게 확인하고 조치를 취할 수 있습니다.

---

### **챗봇 알림 메시지 예시**
<img src="https://github.com/user-attachments/assets/132b5e9b-c93e-41ea-8409-60b92ae40d3a" height=500 width=250>


---

### **작동 원리 요약**
1. **Grove 센서** → 실내 PM2.5 데이터 측정  
2. **에어코리아 OpenAPI** → 실외 PM2.5 데이터 수집  
3. **임계값 비교** → 실내 값이 기준 초과 시 챗봇 작동  
4. **디스코드 서버** → 실시간 알림 전송  
5. **모바일 앱 연동** → 핸드폰에 푸시 알림 도착  



<br>



## 5. 시행착오

- **(1) OpenAI 및 Gradio 버전 호환성 문제**  
    - 주피터 노트북 환경에서 OpenAI와 Gradio 라이브러리의 버전 충돌로 인해 Gradio 챗이 정상적으로 작동하지 않는 문제가 발생하였습니다.  

| Gradio 버전 |
|----------|
| <img src="https://github.com/user-attachments/assets/02e40109-83c3-4f6c-8de0-144b9af3a2e5" height=300 width=300>|

<br>

- **(2) 에어코리아 API 사용의 어려움**  
    - API 호출 시 데이터 요청 형식 및 응답 구조를 파악하는 과정에서 어려움이 있었습니다.  

<br>

- **(3) Gradio 챗봇 연산 함수 설정의 어려움**  
    - 실내 **실시간 측정 값**과 **실외 API 값**을 비교하는 연산 함수를 설정하는 과정이 복잡했습니다.  

<br>

- **(4) 젯슨 나노 카메라와 이미지 데이터 처리 문제**  
    - 젯슨 나노의 카메라를 사용해 문이 열리고 닫힌 상태를 감지하려 했지만, 이미지 처리 구현이 어려웠습니다.  

<br>

- **(5) 디스코드 실내 미세먼지 알림 봇 구현 문제**  
    - 초기에는 휴대폰 디스코드 앱으로 알림이 전달되지 않는 문제가 있었습니다.
  
---

## 5-1. 시행착오 해결 방법

- **(1) OpenAI 및 Gradio 버전 호환성 문제 해결**  
    - Gradio 버전을 **3.0.12**, OpenAI 버전을 **0.8.0**으로 재설치하여 호환성 문제를 해결했습니다.  
    - 버전 재설치 코드:  
    ```bash
    pip install gradio==3.0.12
    pip install openai==0.8.0
    ```
    - 해당 조치를 통해 Gradio 챗과 OpenAI API 호출이 정상적으로 작동하였습니다.

<br>

- **(2) 에어코리아 API 사용의 어려움 해결**  
    - API 명세서를 참고하여 요청 파라미터와 응답 구조를 명확히 파악했습니다.  
    - API 요청 코드 예시:  
    ```python
    import requests

    url = "http://api.airkorea.or.kr"
    params = {"region": "대전", "serviceKey": "YOUR_API_KEY"}
    response = requests.get(url, params=params)
    print(response.json())
    ```

<br>

- **(3) Gradio 챗봇 연산 함수 설정 해결**  
    - 실내외 데이터를 비교하기 위해 Python 함수 내에 연산 로직을 구현했습니다.  
    ```python
    def compare_pm25(indoor, outdoor):
        if indoor > outdoor:
            return "실내 공기질이 더 높습니다. 환기가 필요합니다."
        return "실내 측정값이 더 낮습니다. 창문을 닫으세요"
    ```


<br>

- **(4) 젯슨 나노 카메라 이미지 데이터 처리 방향 수정**  
    - 이미지 데이터 처리가 복잡하고 시간 소모가 커서 미세먼지 측정 및 알림 챗봇 시스템을 구현하였습니다.

<br>

- **(5) 디스코드 실내 미세먼지 알림 봇 문제 해결**  
    - 디스코드 봇의 채널 ID와 메시지 전송 코드를 수정하여 정상적으로 알림이 수신되도록 하였습니다.  
    ```python
    import discord

    TOKEN = "YOUR_BOT_TOKEN"
    CHANNEL_ID = 123456789012345678

    client = discord.Client(intents=discord.Intents.default())

    @client.event
    async def on_ready():
        channel = client.get_channel(CHANNEL_ID)
        await channel.send("✅ 정상: 실내 PM2.5 값이 정상입니다.")
    client.run(TOKEN)
    ```
    - **결과**: 휴대폰 앱에 알림이 정상적으로 수신되었습니다.  


<br>

    
## 6. 개선 방안


- **(1) 정밀한 임계값 설정**
    - 현재 임계값은 경험적 평균값을 기반으로 설정되었으나, 측정 환경과 시간대별 공기질 변화를 반영한 동적 임계값 설정이 필요합니다.  
    - AI 모델을 활용해 장기간의 데이터 학습을 통해 더 정확한 임계값을 예측할 수 있습니다.

- **(2) 실내외 데이터의 상시 모니터링**
    - Grove 센서와 에어코리아 API 데이터를 지속적으로 수집하여 장기적인 패턴 분석이 가능하도록 데이터베이스를 구축이 필요합니다.  
    - 실시간 모니터링뿐만 아니라 과거 데이터 시각화 및 예측 기능을 강화하면 사용자에게 더 유용한 정보를 제공할 수 있습니다.

- **(3) 실외 데이터 API의 추가 확장**
    - 에어코리아 OpenAPI 외에도 다른 공공 데이터 API(예: 환경부, 기상청)를 추가로 활용해 더 다양한 대기질 데이터를 확보합니다.  
    - 이를 통해 측정 오차를 보완하고 지역별 미세먼지 상태를 종합적으로 분석할 수 있습니다.

- **(4) 자동화된 환기 시스템 연동**
    - 디스코드 알림뿐만 아니라, 환기 필요 알림이 발생했을 때 자동으로 공기청정기나 환기 장치를 작동시키는 시스템을 연동합니다.  
    - 이를 위해 IoT 기술을 접목하여 스마트홈 환경에 적용할 수 있습니다.


<br>

## 7. 프로젝트 후기

### 🍊권도현

잘 알지 못했던 아두이노 및 잿슨 나노와의 연동등을 프로젝트를 진행해보면서 경험해볼 수 있어서 재밌는 경험이였고, 환경공학과로서 미세먼지 농도 데이터를 이용해서 프로젝트를 진행한 만큼 의미있었던 시간이였던 것 같습니다.
특히 디스코드를 이용해서 미세먼지 알람을 직접 휴대폰으로 확인할 수 있도록 직접 GPT를 이용해서 코딩을 한 부분은 저에게 새롭게 다가왔고 앞으로 관련 부분의 프로그래밍을 좀 더 배우고자 합니다.
또한 이를 계기로 환경분야와 IT 기술에 대한 관심이 더욱 강해지게 되었습니다. 재미있었습니다~

<br>

### 👻구현준

여러모로 많은 것들을 배울 수 있었던 한 달이었습니다. 혼자서는 할 수 없었던 일이라는 것을 너무 잘 알기에 팀원들에게 정말 감사하다는 말 전하고 싶습니다. 개인적으로 아쉬웠던 부분은 기한 내에 기능을 구현하는 데에만 집중하면서 아두이노나 새로 배웠던 것들을 체계적으로 기록하지 못했다는 점입니다. 이렇게 느낀 바가 있으니 이후의 제가 잘 정리할것이라 믿습니다. 다들 수고하셨습니다!!!!

<br>

### 😎이수현

팀 프로젝트 시작에 앞서 초기 설정을 진행하며 체계적인 설계의 중요성을 느꼈습니다. 앞으로는 점점 더 체계적이고 효율적으로 프로젝트를 진행할 수 있도록 발전하고 싶습니다.
정규 수업 직후에 프로젝트를 진행하면서 배운 내용을 직접 구현하는 과정이 어색했지만 어떤 부분이 부족한지 알 수 있는 기회였습니다. 스스로 최대한 노력해보고 팀원들과 함께 해결해 나가면서 협업의 장점을 체감할 수 있었습니다. 하지만 빠르게 작업을 진행하면서 팀원들과 함께 해결한 이슈가 어떤 이슈이며 어떻게 해결했는지에 대해 자세히 작성하지 못한 것이 아쉽습니다. 조원들 모두에게 고생했다고 전하고 싶습니다🧡

<br>

### 🐬류태안

이번 산업인공지능 젯슨 나노 수업을 통해서 가장 와닿았던 점은 실내 공기청정기의 원리를 알 수 있었다는 점 이었습니다. 내가 직접 미세먼지농도를 측정할 수 있고 간단하지만 공기청정기를 만든 것 같아 의미있던 시간이었던 것 같습니다.
또한 자동으로 저의 핸드폰에 알림이 가는 기능까지 만들 수 있었고 이를 활용하여 잿봇만 있다면 직접 저의 자취방에 설치해보고 싶다는 생각을 했습니다. 자취방의 미세먼지 농도를 측정하면 요리할 때 환기를 해야하는지 알 수 있고, 만약 화재가 일어난다면 제가 외부에 있어도 인지할 수 있을 것 입니다. 이번 시간이 정말 개발자가 된 느낌이었고, 이 경험을 살려 미래에 대기분야에서 직업을 가질 수 있는 기회가 되면 좋겠습니다.
