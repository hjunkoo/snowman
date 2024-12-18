# 🖥️ 미세먼지 측정 README 


<br>

## 프로젝트 소개

- 실내와 실외의 미세먼지 농도를 비교 및 답변하는 그라디오 만들기.
- 실내 미세먼지가 기준치 이상이 될 경우 디스코드 알림 발생.
- 디스코드와 핸드폰 어플 연동해 알림 즉시 확인.
  
<br>

## 팀원 구성

<div align="center">

| **권도현** | **구현준** | **이수현** | **류태안** |
| :------: |  :------: | :------: | :------: |
| <img src="https://github.com/user-attachments/assets/f7665068-667d-4409-bf56-ea39f9b2bf10" height=200 width=130>| <img src="https://github.com/user-attachments/assets/115d6c7c-4e78-4057-8436-fb73508a2dc8" height=200 width=150>| <img src="https://github.com/user-attachments/assets/c40d7b0d-f7b1-4572-bada-710346446bdb" height=220 width=160>| <img src="https://github.com/user-attachments/assets/5ca8c56b-651b-4b1a-9b5a-8d73342d7592" height=200 width=150>|

</div>


<br>


## 1. 응용 기술과 활용방안

### function calling

- **Gradio 및 Arduino**
    - Gradio: 실외 미세먼지 데이터와 Arduino를 통해 수집한 실내 미세먼지 데이터를 비교할 수 있는 인터페이스를 제공하였습니다.
- **OpenAPI**
    - OpenAPI 표준: 에어코리아 API를 통해 실외 미세먼지 데이터를 가져올 때 OpenAPI 스펙을 활용하여 API의 구조와 동작 방식을 구현하였습니다.
    
### discord

- **디스코드 연동**
   - 실내 미세먼지 값이 설정한 임계값을 초과할 경우, Discord API를 활용하여 챗봇이 자동으로 알림을 전송하도록 구현하였습니다.
- **알림 메시지**
   - 알림 내용에는 실내 미세먼지 값과 함께 "환기가 필요합니다"라는 메시지가 포함되며, 실외 미세먼지 값도 함께 제공하여 사용자가 환기 여부를 판단할 수 있도록 도왔습니다.


<br>



## 2. 역할 분담

### 🍊권도현
- **역할**
    - 전체 코드 구현
    - 디스코드 알림봇 생성
    - Github 작성

<br>

### 👻구현준
- **역할**
    - 발표
    - OpenAPI 코드 구현

<br>

### 😎이수현
- **역할**
    - 전체 코드 구현
    - 디스코드 알림봇 생성
    - Github 작성

<br>

### 🐬류태안
- **역할**
    - PPT 제작
    - OpenAPI 코드 구현
    
<br>

## 3. 프로젝트 기간 및 측정 장소

### 프로젝트 기간

- 전체 프로젝트 기간 : 2024-12-01 ~ 2025-12-19

<br>

### 측정 장소

- 충남대학교 공대 3호관 515호 환경공학과 학생회실
- 주간회의를 진행하며 작업 순서와 방향성에 대한 고민을 나누었습니다.

<br>

## 4. 프로젝트 세부내용

## (1) 응용 기술과 활용방안

### [측정 기기 및 데이터 수집]
- 이번 프로젝트에서는 실내 및 실외 미세먼지 데이터를 실시간으로 측정 및 분석하기 위해 다음과 같은 기술과 장치를 활용하였습니다
    - **실내 미세먼지 측정**: 
        - **아두이노(Arduino)**에 Grove 센서를 연결하여 실내 미세먼지 상태를 실시간으로 측정하였습니다.
        - 센서를 통해 수집된 데이터를 디스코드 알림 시스템과 연계하여 환기 필요성을 사용자에게 알렸습니다.
    - **실외 미세먼지 데이터 수집**: 
        - 에어코리아 API를 활용하여 실외 미세먼지 농도를 가져왔습니다.
        - OpenAPI 스펙을 기반으로 function calling을 구현하여 데이터를 효율적으로 요청하고, 응답 데이터를 구조화하였습니다.
        - 실내외 데이터를 비교 분석하여 더 나은 의사 결정을 지원했습니다.

### [데이터 시각화 및 사용자 인터페이스]
- **Gradio**:
    - Gradio를 활용해 실내와 실외 미세먼지 데이터를 직관적으로 확인할 수 있는 사용자 인터페이스(UI)를 구축하였습니다.
    - 사용자 입력을 통해 실시간 데이터를 분석하거나 과거 데이터를 시각적으로 비교할 수 있는 기능을 제공하였습니다.
- **디스코드 연동**:
    - 디스코드 API를 사용하여, 실내 미세먼지 값이 특정 임계치를 초과할 경우 사용자에게 "환기가 필요합니다"라는 알림을 자동으로 전송하는 시스템을 구현하였습니다.

### [function calling]
- **자동화 및 효율성**:
    - function calling 기법을 적용해 데이터를 요청하고 처리하는 작업을 자동화하였습니다.
    - 아두이노 Grove 센서 데이터와 에어코리아 API 데이터의 통합 분석을 지원하여, 사용자에게 실시간으로 유용한 정보를 제공합니다.

<br>

## (2) Grove 기기의 세부적인 특성 및 연결 방법

- **Grove 센서 시스템**:
    - **모듈화 설계**: Grove 센서는 플러그 앤 플레이 방식을 지원하여 아두이노와 손쉽게 연결할 수 있습니다.
    - **미세먼지 측정**: PM2.5 및 PM10과 같은 입자 크기를 기반으로 실내 공기질 데이터를 정밀하게 측정합니다.

- **Grove 센서 연결 방법**:
    - 아래 이미지처럼 Grove 센서와 아두이노 UNO를 연결하여 데이터를 수집하였습니다.
    
| 회로도 |
|----------|
|(![image](https://github.com/user-attachments/assets/de3fe5e8-9d60-409f-9d32-eb0ca83c07f3))|

    - **핀 연결**:
        - **빨간색 (VCC)**: 5V 핀
        - **검은색 (GND)**: GND 핀
        - **노란색 (DATA)**: 아날로그 핀 A0
        - **녹색 (NC)**: 사용하지 않음

---

- **이번 프로젝트에서 활용**:
    - 센서를 통해 수집된 데이터는 실시간으로 분석되며, 디스코드 알림 시스템을 통해 사용자에게 환기 필요 여부를 알려주었습니다.
    - Gradio UI를 통해 직관적으로 실내외 미세먼지 데이터를 응답하고 비교할 수 있도록 구현하였습니다.


<br>

## (3) 에어코리아 OpenAPI의 특징 및 활용

- **에어코리아 OpenAPI 특징**:
    - **공공 데이터 제공**: 에어코리아 OpenAPI는 국내 실외 대기질 정보를 실시간으로 제공하는 공공 데이터 플랫폼입니다.
    - **다양한 대기질 항목**: 미세먼지(PM10), 초미세먼지(PM2.5), 오존(O3), 이산화질소(NO2) 등 다양한 대기 오염 물질의 농도를 조회할 수 있습니다.
    - **지역별 데이터 제공**: 특정 지역(시·군·구 단위)의 실시간 대기질 정보를 API 호출을 통해 가져올 수 있습니다.

- **프로젝트에서의 활용**:
    - **대전지역 PM2.5 데이터 수집**:
        - 에어코리아 OpenAPI를 사용해 대전 지역의 초미세먼지(PM2.5) 농도를 실시간으로 가져왔습니다.
        - API를 통해 받은 실외 PM2.5 값과 Grove 센서를 통해 수집한 실내 PM2.5 값을 비교 분석하였습니다.

- **데이터 수집 방법**:
    - **Function Calling**:
        - OpenAPI의 요청 및 응답 구조를 기반으로 function calling 기법을 적용하여 데이터를 효율적으로 가져왔습니다.
        - 요청 시 대전 지역 코드를 파라미터로 전달하여 해당 지역의 PM2.5 값을 조회.
    - **데이터 활용**:
        - 수집된 실외 PM2.5 값은 실내 값과 함께 분석되어 Gradio UI를 통해 시각적으로 표현되었습니다.
        - 디스코드 알림 시스템과 연계하여, 실내 미세먼지 값이 기준치를 초과한 경우 실외 미세먼지 상태를 함께 제공하여 사용자가 환기 필요 여부를 판단할 수 있도록 지원하였습니다.

### Google Colab 코드
에어코리아 OpenAPI와 실내 데이터를 비교 분석한 코드는 아래 링크에서 확인할 수 있습니다.  
👉 [Google Colab 코드 보기](https://colab.research.google.com/drive/1uO17q-Awr4OyG6uBWWWZX9RbH9WJGxBQ)


---

- **결과**:
    - **실내-실외 데이터 비교**: 
        - 실내 PM2.5 값이 기준치를 초과하면, 실외 PM2.5 데이터를 확인하여 환기 여부를 판단할 수 있었습니다.
    - **사용자 알림 시스템**:
        - 디스코드 챗봇을 통해 환기 필요 메시지를 실시간으로 사용자에게 전달하였습니다.


<br>





## 5. 시행착오

- [접근제한 설정](https://github.com/likelion-project-README/README/wiki/README-6.%EC%8B%A0%EA%B2%BD-%EC%93%B4-%EB%B6%80%EB%B6%84_%EC%A0%91%EA%B7%BC%EC%A0%9C%ED%95%9C-%EC%84%A4%EC%A0%95)

- [Recoil을 통한 상태관리 및 유지](https://github.com/likelion-project-README/README/wiki/README-6.%EC%8B%A0%EA%B2%BD-%EC%93%B4-%EB%B6%80%EB%B6%84_Recoil%EC%9D%84-%ED%86%B5%ED%95%9C-%EC%83%81%ED%83%9C%EA%B4%80%EB%A6%AC-%EB%B0%8F-%EC%9C%A0%EC%A7%80)
  
<br>

## 6. 개선 방안

- API 모듈화 : API를 불러오는 코드의 반복이 많아 모듈화할 예정
- lighthouse Performance 증진
    - 모든 페이지에서 특히 Best Practices & SEO 점수는 90~100으로 우수
    - Performance 점수가 대체적으로 미흡한 문제
    
    ![KakaoTalk_Photo_2023-01-04-16-55-30](https://user-images.githubusercontent.com/112460466/210591134-09bf8efd-3c34-4b99-a3d7-895ca99e1457.png)
    
- **23-01-17 성능 개선 내용**
    
    ![성능개선 후](https://user-images.githubusercontent.com/106502312/212872369-7ceeb2cf-d551-41d2-bfb0-01e35e9903fe.png)
    
    - 이미지 최적화
        - `<img>` 요소에 `width` , `height` 속성값을 명시해 불필요한 Reflow를 방지했습니다.
        - browser-image-compression 라이브러리를 사용해 유저가 업로드하는 이미지를 압축했습니다.
        - Intersection Observer API를 사용해 Lazy Loading 기법을 적용하여 홈 피드의 게시글 이미지가 viewport 내에 들어오는 순간 로딩되도록 변경했습니다.
    - 웹폰트 최적화
        - WOFF2 포맷을 추가하고 가장 우선적으로 적용되도록 선언했습니다.
        - 서브셋 폰트로 교체해 용량을 줄였습니다.
    
<br>

## 7. 프로젝트 후기

### 🍊권도현

깃헙을 통한 협업에 익숙해지는 것, 서로 감정 상하지 않고 무사히 마무리하는 것이 1차적인 목표였어서 항상 이 부분을 명심하면서 작업했습니다.
각자 페이지를 작업하고 합치는 과정에서 마주친 버그들이 몇 있었는데, 시간에 쫓기느라 해결하기에 급급해서 제대로 트러블슈팅 과정을 기록하지 못한 게 살짝 아쉬운 부분으로 남습니다. 그래도 2022년 한 해 동안 가장 치열하게 살았던 한 달인 것 같습니다. 조원들 모두에게 고생했다고 전하고 싶습니다🧡

<br>

### 👻구현준

여러모로 많은 것들을 배울 수 있었던 한 달이었습니다. 혼자서는 할 수 없었던 일이라는 것을 너무 잘 알기에 팀원들에게 정말 감사하다는 말 전하고 싶습니다. 개인적으로 아쉬웠던 부분은 기한 내에 기능을 구현하는 데에만 집중하면서 트러블 슈팅이나 새로 배웠던 것들을 체계적으로 기록하지 못했다는 점입니다. 이렇게 느낀 바가 있으니 이후의 제가 잘 정리하면서 개발할 거라 믿습니다… 하하 다들 수고하셨습니다!!!!

<br>

### 😎이수현

팀 프로젝트 시작에 앞서 초기 설정을 진행하며 체계적인 설계의 중요성을 느꼈습니다. 앞으로는 점점 더 체계적이고 효율적으로 프로젝트를 진행할 수 있도록 발전하고 싶습니다.
정규 수업 직후에 프로젝트를 진행하면서 배운 내용을 직접 구현하는 과정이 어색했지만 어떤 부분이 부족한지 알 수 있는 기회였습니다. 스스로 최대한 노력해보고 팀원들과 함께 해결해 나가면서 협업의 장점을 체감할 수 있었습니다. 하지만 빠르게 작업을 진행하면서 팀원들과 함께 해결한 이슈가 어떤 이슈이며 어떻게 해결했는지에 대해 자세히 작성하지 못한 것이 아쉽습니다.
’멋쟁이 사자처럼’이라는 같은 목표를 가진 집단에서 프로젝트에 함께할 수 있는 소중한 경험이었습니다. 함께 고생한 조원들 모두 고생하셨습니다! 앞으로도 화이팅해서 함께 목표를 이뤄가고 싶습니다.

<br>

### 🐬류태안

컨벤션을 정하는 것부터 Readme 파일 작성까지 전 과정을 진행하려니 처음 생각보다 많은 에너지를 썼어요. 좋은 의미로 많이 썼다기보다, 제 능력을 십분 발휘하지 못해서 아쉬움이 남는 쪽입니다. 개발한다고 개발만 해서는 안 된다는 것을 몸소 느껴보는 기간이었던 것 같습니다. 이번 기회로 프로젝트를 진행하면서, 제가 잘하는 점과 부족한 점을 확실하게 알고 가는 건 정말 좋습니다. 기술적인 부분에 있어서는 리액트의 컴포넌트화가 주는 장점을 알았습니다. 조금 느린 개발이 되었을지라도 코드 가독성 부분에 있어서 좋았고, 오류가 발생해도 전체가 아닌 오류가 난 컴포넌트와 근접한 컴포넌트만 살펴보면 수정할 수 있는 부분이 너무 편했습니다. 모두 고생 참 많으셨고 리팩토링을 통해 더 나은 프로젝트 완성까지 화이팅입니다.
