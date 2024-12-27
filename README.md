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

## (4) Details of Discord Chatbot Notification System

- **Create a Discord chatbot**
  - **Bot creation**: Discord Developer Portal created a chatbot for the project.
  - **Token issued**: Bot tokens have been issued for communication between chatbot and server, and have been applied to code.
  - **Set Bot ID**: Invited the generated chatbot to the Discord server, set the corresponding bot ID and linked it to the project.

- **Implementation of notification system**
  - **Set thresholds**
    - The threshold value was set arbitrarily through experiments after empirically analyzing the average value in consideration of the characteristics of the measurement place.
    - If the reference value is exceeded, a notification will sound, and if it is within the normal range, a normal message will be sent.

  - **Notify when thresholds are exceeded**
    - If the indoor PM2.5 value measured by the Grove sensor exceeds the set threshold, a notification is automatically sent to the Discord server.
    - The message includes the indoor PM2.5 value and the outdoor PM2.5 value (Air Korea API data) together, and has been implemented to make it easier for users to determine whether ventilation is present or not.


  - **Connect to Discord servers**
    - Using Python's 'discord.py ' library, we connected chatbots to the server and implemented a real-time message transmission function.
    - Indoor air quality status and ventilation required messages are output to the set server channel.

  - **Connects mobile phone notifications**
    - The Discord mobile app also delivers real-time notifications to users' phones.
    - This allows users to quickly check indoor fine dust conditions anytime, anywhere and take action.

---

### **Example Chatbot notification message**
<img src="https://github.com/user-attachments/assets/132b5e9b-c93e-41ea-8409-60b92ae40d3a" height=500 width=250>


---

### **Summary of operating principles**
1. **Grove sensor** → indoor PM2.5 data measurement
2. **AirKorea OpenAPI** → outdoor PM2.5 data collection
3. **Comparison of thresholds** → Chatbot operated when indoor values exceed criteria
4. **Discord server** → Send real-time notifications
5. **Mobile app linked** → Push notification arrives on your phone



<br>



## 5. trial and error

- **(1) OpenAI and Gradio Version Compatibility Issues**
    - In Jupiter laptop environment, the version conflict between OpenAI and the Gradio library caused the Gradio Chat to not function properly. 

| Gradio version |
|----------|
| <img src="https://github.com/user-attachments/assets/02e40109-83c3-4f6c-8de0-144b9af3a2e5" height=300 width=300>|

<br>

- **(2)Difficulty using Air Korea API**
    - There were difficulties in identifying the data request format and response structure when calling API.  

<br>

- **(3) Difficulty in setting up the Gradio Chatbot operation function**
    - The process of setting up an operational function to compare indoor **real-time measurements** and **outdoor API values** was complicated. 

<br>

- **(4) Jetson Nano Camera and Image Data Processing Problems**
    - I tried to detect the door opening and closing using Jetson Nano's camera, but it was difficult to implement the image processing. 

<br>

- **(5) Discord Indoor Fine Dust Notification Bot Implementation Problems**
    - In the beginning, there was a problem that notifications were not delivered to the phone Discord app.
  
---

## 5-1. trial and error solution

- **(1) Troubleshooting OpenAI and Gradio version compatibility**
    - Reinstalling the Gradio version to **3.0.12** and the OpenAI version to **0.8.0** resolved the compatibility issue.
    - Version reinstall code:
```bash
        pip install gradio==3.0.12
        pip install openai==0.8.0
```
    - This action enabled the Gradio Chat and OpenAI API calls to function normally.
<br>

- **(2) Addressing the difficulties of using Air Korea API**
    - I clearly identified the request parameters and response structure by referring to the API specification.
    - API request code example:
    ```python
    import requests

    url = "http://api.airkorea.or.kr"
    params = {"region": "대전", "serviceKey": "YOUR_API_KEY"}
    response = requests.get(url, params=params)
    print(response.json())
    ```

<br>

- **(3) Resolving the Gradio Chatbot operation function settings**
    - To compare indoor and outdoor data, we have implemented computational logic within Python functions.
    ```python
    def compare_pm25(indoor, outdoor):
        if indoor > outdoor:
            return "실내 공기질이 더 높습니다. 환기가 필요합니다."
        return "실내 측정값이 더 낮습니다. 창문을 닫으세요"
    ```


<br>

- **(4) Modifying the direction of Jetson Nano Camera Image Data Processing**
    - We implemented a fine dust measurement and notification chatbot system because image data processing is complicated and time consuming.

<br>

- **(5) Troubleshooting Discord Indoor Fine Dust Notification Bot**
    - I modified the channel ID and message sending code of the Discord bot to ensure that the notification was received normally. 
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

    
##6. an improvement plan


- **(1) Precise threshold setting**
    - Current thresholds are based on empirical mean values, but dynamic thresholds are required to reflect changes in air quality over time and in the measurement environment.
    - Using AI models, long-term data learning can predict more accurate thresholds.

- **(2) Continuous monitoring of indoor and outdoor data**
    - It is necessary to establish a database to enable long-term pattern analysis by continuously collecting Grove sensor and Air Korea API data.
    - As well as real-time monitoring, enhancing historical data visualization and prediction can provide more useful information for users.

- **(3) Further expansion of outdoor data APIs**
    - In addition to Air Korea OpenAPI, other public data APIs (e.g., Ministry of Environment, Korea Meteorological Administration) are used to obtain more diverse air quality data.
    - Through this, measurement errors can be supplemented and fine dust conditions by region can be comprehensively analyzed.

- **(4) Integrating an automated ventilation system**
    - In addition to the Discord notification, it connects a system that automatically activates an air purifier or ventilation device when a ventilation requirement notification occurs.
    - To this end, IoT technology can be combined and applied to smart home environments.


<br>

## 7. Review of the project

### 🍊Kwon Do-hyeon

It was a fun experience to experience interworking with Arduino and Jatson Nano, which I did not know well, and it was a meaningful time as I worked on the project using fine dust concentration data as an environmental engineering department.
In particular, the part that I coded using GPT directly so that I can check the fine dust alarm on my phone using Discord has come to me anew, and I would like to learn more about programming related parts in the future.
It also increased my interest in the environmental field and IT technology. It was fun

<br>

### 👻Koo Hyeon-jun

It was a month where I was able to learn a lot of things in many ways. I want to say thank you to the team members because I know so well that I couldn't do it alone. Personally, what I felt sorry about was that I couldn't systematically record Arduino or new things I learned while focusing only on implementing functions within the deadline. I've felt this way, so I believe I'll organize it well in the future. Thank you all for your hard work!!!!

<br>

### 😎Lee Soo-hyeon 

Prior to the start of the team project, I felt the importance of systematic design as I proceeded with the initial setting. In the future, I want to develop so that I can proceed with the project more and more systematically and efficiently.
Immediately after the regular class, the process of directly implementing what you learned while working on the project was awkward, but it was an opportunity to know what was lacking. I was able to feel the advantages of collaboration as I tried my best and solved it with my team members. However, it is unfortunate that I could not write in detail what issues I solved with my team members and how I solved them as I proceeded quickly. I would like to say to all of my team members that you worked hard. 🧡

<br>

### 🐬Ryu Tae-an

What touched me the most through this industrial artificial intelligence Jetson nano class was that I was able to know the principle of indoor air purifiers. I can measure the concentration of fine dust myself and it is simple, but I think it was a meaningful time because I made an air purifier.
Also, I was able to create a function that automatically alerts my phone, and I thought that I would like to install it in my own room if I had a Zabot by using it. By measuring the concentration of fine dust in my own room, I could see if I had to ventilate when cooking, and if a fire broke out, I could recognize it even if I was outside. I really felt like a developer this time, and I hope this will be an opportunity to use this experience to get a job in the air field in the future.
