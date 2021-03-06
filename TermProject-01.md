
#컴퓨터 시스템 기초 설계  

##컴퓨터 시스템 기초설계 1조
#####2008135010 김광수
#####2010136012 김경준
#####2010136048 박성균
#####2010136074 양형모

----------------------------------

### **최종 보고서 목차**
##### 1-1. 문제 정의하기 사례
##### 1-2. 필요성
##### 1-3. 목표
##### 1-4. 요구사항
##### 2-1. 요구사항을 충족시키기 위한 아이디어
##### 2-2. 기존 유사 아이디어
##### 2-3. 기존 유사 아이디어와 차이점
##### 2-4. 우리 아이디어의 장점
##### 3-1. 시스템 목적
##### 3-2. 시스템 구조
##### 3-3. 시스템 기능
##### 3-4. 시스템 구성 요소
##### 3-5. 시스템 구성 요소 간 동작 흐름
##### 4-1. 실험 및 평가의 목적
##### 4-2. 시스템 설계 과정의 실험
##### 4-3. 실험의 분류
##### 4-4. 실험의 종류 - 실제 구현 후 실험을 한다면
##### 4-5. 실험의 범위
##### 4-6. 대조군
##### 4-7. 평가 지표
##### 4-8. 독립 변수, 종속 변수
##### 4-9. 결과 분석과 해석
----------------------------------
##**1-1. 문제 정의하기 사례**
  - 최초로 인식된 문제 정의  
  : 교통 사고율이 증가하기 때문에 새로운 보행자 안전 시스템을 도입하자.

  - 문제 요약  
     : 보행 중 스마트폰 사용 부주의로 인한 사고에 대한 방안이 미흡하다.

  - 왜라는 질문과 답 반복 (5whys → 3whys)

|질문과 답              |                                                                                                         |
|:----------------------|:------------------------------------------------------------------------------------------------------- |
| 질문                  | 왜 새로운 보행자 안전 시스템을 도입하는가?                                                              |
| 답                    | 교통사고율을 감소시키기 위해.                                                                           |
|수정된 진짜 문제 정의문| 교통사고율을 감소시키기 위해 새로운 보행자 안전 시스템을 도입하자                                       |
| 질문                  | 왜 교통사고율을 감소시키는가?                                                                           |
| 답                    | 특정 지점에서 교통사고가 자꾸 발생하기 때문에                                                           |
|수정된 진짜 문제 정의문| 특정 지점에 교통사고를 감소하기 위해 새로운 보행자 안전 시스템을 도입하자.                              |
| 질문                  | 왜 특정 지점에서 사고가 발생하였는가?                                                                   |
| 답                    | 보행 중 스마트폰을 사용했기 때문에                                                                      |
|수정된 진짜 문제 정의문| 보행 중 스마트폰 사용 시 부주의로 인한 교통사고를 줄이기 위한 새로운 보행자 안전 시스템을 모색해야 한다.|


**진짜 문제 정의**  
  : 보행 중 스마트폰 사용 시 부주의로 인한 교통사고를 줄이기 위한 새로운 보행자 안전 시스템을 모색해야 한다.

========================================

##**1-2. 필요성**
![필요성1](http://postfiles9.naver.net/20151211_280/yhm1104_144981242933926jLV_JPEG/1-2_(1).JPG?type=w2)
![필요성2](http://postfiles2.naver.net/20151211_161/yhm1104_1449812442513sWTjX_JPEG/1-2_(2).JPG?type=w2)
![필요성3](http://postfiles6.naver.net/20151211_69/yhm1104_1449812448084lS1Gd_JPEG/1-2_(3).JPG?type=w2)
   
========================================

##**1-3. 목표**  
  : 보행자 교통 사고율을 감소시키기 위해 도로에 있는 해당 어플리케이션을 사용하는 사용자에게 푸쉬 알림과 진동을 제공한다. 그리고 교통사고가 잦은 지역이나 위험한 지역에 비콘을 설치하여, 사용자에게 알림을 전송하여 위험 상황을 인지시킨다.

========================================

##**1-4. 요구사항**
 - 어플리케이션 설치를 유도해야 한다.
 - 위험지역으로 지정되거나 판단되는 구역에 비콘을 설치한다.
 - 위험이 예상되는 상황과 그렇지 않은 상황을 구분해야한다.
 - 위험이 예상되는 사용자에게 알림을 주어야한다.

------------------------------------
====================================

##**2-1. 요구사항을 충족시키기 위한 아이디어**
#####**Q1. 어플리케이션 설치를 유도해야 한다.**
 - **어플리케이션에 대한 거부감 최소화**  
 → 학생들 같은 경우에는 학교의 지시나 부모님의 권유로 어플리케이션을 설치하도록 하고, 성인 같은 경우에는 흥미로운 컨텐츠나 뉴스 등을 가지고 와서 접근하기 쉽게 만들어서 어플리케이션에 대한 거부감을 줄이도록 하는 것을 방법으로 꼽았습니다.  


#####**Q2. 위험지역으로 지정되거나 판단되는 구역에 비콘을 설치해야 한다.**
- **유사 사고 발생지역 파악**  
    → 급커브 지역이나 사각지대에 잇는 보행자에게 메시지를 전달하는 방법도 있지만 가장 우선적으로 기존에 보행자가 스마트폰을 사용하면서 다니다 교통사고가 난 지점을 먼저 파악하고, 그 지점에서 교통사고의 빈도수에 따라 위험 알림 메시지를 전달하도록 할 것입니다.  


#####**Q3. 위험이 예상되는 상황과 그렇지 않은 상황을 구분해야 한다.**
- **차량의 속도에 따른 위험상황 계산**  
    → 횡단보도로부터 50m 정도 떨어진 곳에 스피드건을 설치합니다. 차량이 스피드건을 지나칠 때의 속도를 측정하여 지정속도를 초과하면 비콘에게 정보를 전달하고 비콘은 다시 사용자에게 알림을 주는 식으로 차량의 속도에 따라 위험이 예상되는 상황과 그렇지 않은 상황을 구분할 수 있다고 생각합니다.  

#####**Q4. 위험이 예상되는 사용자에게 알림을 주어야 한다.**
- **사용자의 나이에 따른 위험상황 최소화**  
    → 어플리케이션에서 사용자의 나이와 성별을 입력 받도록 설정을 합니다. 나이가 많은 중년층과 노년층은 젊은 사람들 보다 비교적 운동 능력이 떨어진다고 판단하였습니다. 따라서 중년층과 노년층은 다른 연령층보다 알림 메시지를 받는 제한을 조금 더 낮추어서 위험상황을 알리는 정보에 조금 더 쉽게 노출되도록 할 것입니다.  

========================================

##**2-2. 기존 유사 아이디어**
**(1) 도로 위험상황 예보 서비스**  
-  : 운전자에게 필요한 도로 위의 정보를 신속/정확하게 알려주고, 교통사고 빅데이터를 분석하여 유형 별로 나누어 실시간으로 운전자에게 알려주어 안전하게 운행할 수 있도록 도와주는 시스템.  
  
**(2) NFC를 이용한 위험 알림 서비스**  
-  : NFC 밴드를 활용하여 위험 상황이 발생되면 사용자가 스마트폰에 NFC 밴드를 접촉하여 사용자가 미리 지정한 휴대전화 번호로 긴급 메시지를 전송하여 상대방이 메시지에 나와 있는 URL을 통해 메시지 발신자의 위치를 지도로 확인할 수 있다.  

========================================

##**2-3. 기존 유사 아이디어와의 차이점**  
**(1) 도로 위험상황 예보 서비스**  
- 보행자가 아닌 운전자를 위한 교통 정보 서비스 시스템.  
- 돌발상황이 발생하면 현장에 있는 교통경찰관이 직접 정보를 입력하는 방식.  
- 보행자의 안전이 아닌 운전자의 입장에서 빠르고 안전한 길을 알려주는 것이 주 목적  
  
**(2) NFC를 이용한 위험 알림 서비스**  
- 사고를 예방하는 것이 아니라 사고 발생 후 메시지를 전달하는 방식  
- 교통사고를 목적으로 둔 것이 아니라 납치, 성폭행 방지 등을 우선순위로 두고 만든 서비스.  

========================================
  
##**2-4. 우리 아이디어의 장점**  
    - 사람의 안전이라는 중요한 문제와 연관되어 있고 사고를 예방할 수 있다는 점에서 실효성이 크다.  
    - 사용자들은 어플리케이션만 설치한다면 알림을 받을 수 있어 간단히 접근할 수 있다.  
    - 교통정보 시스템에 도입된다면, 사업적 가치 또한 클 것으로 예상된다.  


------------------------------------
====================================

##**3-1. 시스템 목적**  
 : 스마트폰 사용 부주의로 인한 사고 발생률을 줄이기 위해, 도로상의 위험 상황 알림 시스템을 사용하여 사고 발생률을 줄이고 보행자의 안전을 지킬 수 있게 한다.
    
========================================

##**3-2. 시스템 구조**
![시스템전체흐름](http://postfiles3.naver.net/20151211_2/yhm1104_1449812453282lqMnq_JPEG/3-2_(1).JPG?type=w2)

========================================

##**3-3. 시스템 기능**  
  ① 차량 속도 측정 기능  
  ② 보행자 위치 측정 기능  
  ③ 메시지 전송 기능  
  ④ 알림 설정 기능  

========================================

##**3-4. 시스템 구성 요소**  

① 스피드건  
     1) 구성 요소의 기능  
        - 차량 속도 측정  
        - 비콘에 측정 속도 전송  
     2) 입ㆍ출력 데이터  
        - 입력 데이터 : 차량의 움직임  
        - 출력 데이터 : 차량의 속도  

② 비콘  
     1) 구성 요소의 기능  
        - 데이터 송수신  
     2) 입ㆍ출력 데이터  
        - 입력 데이터 : 차량 속도, 보행자의 위치, 위험상황 알림 메시지  
        - 출력 데이터 : 위험 상황 알림 메시지  

③ 서버  
     1) 구성 요소의 기능  
        - 데이터 처리 및 송수신  
     2) 입ㆍ출력 데이터  
        - 입력 데이터 : 차량 속도, 보행자의 위치  
        - 출력 데이터 : 위험 상황 알림 메시지  

④ 모바일 어플리케이션  
     1) 구성요소의 기능  
        - 알림 수신  
        - 사용자의 위치 전송  
     2) 입ㆍ출력 데이터  
        - 입력 데이터 : 위험 상황 알림 메시지  
        - 출력 데이터 : 사용자의 정보 및 사용자의 위치  

========================================

##**3-5. 시스템 구성 요소 간 동작 흐름**

![부분동작1](http://postfiles15.naver.net/20151211_206/yhm1104_1449812459068rUp5c_JPEG/3-5_(1).JPG?type=w2)
- 스피드건으로 차량의 속도를 측정함.  
- 측정된 속도는 비콘으로 측정함.  
- 측정 속도를 전달 받은 비콘은 다시 서버로 전송함.  

----------------------------------------------------



![부분동작2](http://postfiles7.naver.net/20151211_214/yhm1104_1449812462983Ru1V9_JPEG/3-5_(2).JPG?type=w2)
- 모바일 어플리케이션이 GPS를 수신함.  
- GPS를 통하여 얻은 사용자 위치와 사용자 정보를 비콘에 전달함.  
- 위치 정보와 사용자 정보를 전달받은 비콘은 다시 서버로 전송  

---------------------------------------------------


![부분동작3](http://postfiles12.naver.net/20151211_27/yhm1104_1449812465973Mxysn_JPEG/3-5_(3).JPG?type=w2)
- 위험 상황 발생시 비콘에 알림 메시지를 전송함.  
- 비콘은 서버로부터 전달 받은 알림 메시지를 모바일 어플리케이션을 통해 사용자에게 전송함.  

---------------------------------------------------

![부분동작4](http://postfiles11.naver.net/20151211_90/yhm1104_1449812478685OqpT5_JPEG/3-5_(4).JPG?type=w2)
- 강수량 정보를 서버가 받는다.  
- 비콘에서 차량의 속도, 사용자 위치 등을 전달 받는다.  
- 서버는 전달 받은 정보를 활용하여 상황에 맞는 위험 상황 거리 산출과 메시지를 생성함.  

---------------------------------------------------

-------------------------------------


##**4-1. 실험 및 평가의 목적**
- 실험결과로 무엇을 보여줄 것인가?
- 실험결과로 무엇을 주장할 것인가?  
 : 보행중의 스마트폰 부주의로 인한 교통사고를 방지하기 위한 시스템이다. 보행자가 스마트폰을 사용하고 있어, 교통상황을 인지하고 못하고 있을 때, 이 시스템의 알림을 받고 위험상황을 인지, 교통사고를 방지하는 모습을 보여줄 수 있을 것이다.  
 : 이 실험 결과를 토대로 시스템의 도입을 활성화, 교통사고 발생률을 낮추고, 인명 피해를 줄일 수 있을 것으로 보인다.
     
------------------------------------

##**4-2. 시스템 설계 과정의 실험**
- 개발 과정 중의 실험  
: 사용자 설정을 통한 위험도가 실제 상황의 위험도와 유사한지에 대한 시험  
: 거리 계산에 대한 오차율이 정확한지에 대한 실험  
: 시스템 요구사항을 더 잘 이해하기 위한 실험 (보행자 관찰, 감속 구간에서의 감속 여부 등)  

- 개발 후 시스템(혹은 서비스)의 성능 평가를 위한 실험  
- 시스템/서비스의 작동 여부  
: 스피드건, 비콘, 서버, 어플리케이션의 정상 작동 여부 파악  

- 시스템/서비스의 성능  
: 서버가 얼마나 계산을 정확하고 빠르게 하는지에 대한 실험  
: 비콘이 범위안의 사용자를 잘 인지하는지에 대한 실험  

- 시스템/서비스의 사용자 수용 여부  
: 비콘안의 범위에 들어온 사용자에게 메시지 브로드캐스트  

------------------------------------

##**4-3. 실험의 분류**
- 시스템의 기술적인 특징이나 기능 측면 - 시스템 스터디  
: 정확도, 초당 데이터 전송량 측정, 범위 안에 있는 사용자의 수에 따른 알림 메시지 수신 응답 시간  
(비콘의 범위 오차율에 대한 정확도는 얼마인가?, 서버의 계산시간은 얼마인가?, 사용자 위치 인식에 대한 정확도는 얼마인가?, 서버의 초당 데이터 전송량은 얼마인가?)

------------------------------------

##**4-4. 실험의 종류 - 실제 구현 후 실험을 한다면**
어떤 환경에서 동작을 시킬 것인가? 실제 deployment 환경  
: 실험을 위한 시스템 input은 어떻게 만들 것인가? 실제 시스템 이용 환경의 입력 데이터 

------------------------------------

##**4-5. 실험의 범위**
####**시스템의 구성 요소 별 실험**  
- 시스템 구성 요소 별로 기능적/비기능적 요구 사항에 대한 평가를 나누어서 할 수 있음

- **스피드건**  
    → 기능적 요구사항 : 차량의 속도를 정확히 측정하는가?  
    → 비기능적 요구사항 : 차량의 속도를 정확히 측정할 장소에 설치되어 있는가?  

- **비콘**  
    → 기능적 요구사항 : 데이터의 송수신을 신속하고 정확하게 수행하는가, 지정된 범위만을 포함할 수 있게 전력 조절이 잘 되었는가?  
    → 비기능적 요구사항 : 교통 상황에 맞는 적절한 위치에 설치되어 있는가?  

- **서버**  
    → 기능적 요구사항 : 날씨와 노면의 상태를 제대로 계산하고 데이터를 정확하고 신속하게 전송하는가?  
    → 비기능적 요구사항 : 없음.  

- **어플리케이션**  
    → 기능적 요구사항 : 데이터를 전달받고 위험상황에 신속히 알람을 띄울 수 있는가?    
    → 비기능적 요구사항 : 모든 연령을 대상으로 하는 만큼 설치와 절차가 간단해야하고, 모든 스마트폰에서 오류 없이 작동해야한다.  


***End-to-end 시스템 실험***  
전체적인 시스템의 기능적/ 비기능적 요구사항 관점에서의 평가  
기능적 요구사항: 위험 상황 시 신속하고 빠르게 메시지 알림을 전송, 보행자가 인지할 수 있게 하는가?  
비기능적 요구사항 : 알림 방지 어플리케이션이 작동할 수 있는 환경이어야 함 (구성요소 설치/미설치 인지)  

------------------------------------

##**4-6. 대조군**

- 같은 목적을 위한 다른 시스템과 비교

: GPS와 비콘 비교
: gps를 이용할 때 보다 비콘을 이용하면 오차 범위가 줄어들고, 정확성이 향상된다.  

|	비교 항목	|	GPS	     |	 Beacon			|
|:----:|:----:|:----:|
|인식 범위	|	좁음	     |	5 cm ~ 최대 50 m (넓음) |
|오차 범위 	|	수 ~ 수십 m  | 	5 ~ 10 cm		|
|설치 가능	|	실외	     |	실내/외			|
|전력 소모	|	 -	     |	작음			|
|정확성		|	낮음	     |	높음			|

:비콘이 기존의 통신 기술에 비해 거리가 비약적으로 늘어났고, 5~45cm의 넓은 거리를 감지할 수 있으면서도 오차가 작은 위치 기반 블루투스이다. 인식범위가 넓고 위치 파악이 GPS보다 정확한 강점을 갖고 있다. 또한 전력 소모가 작으며, 작은 동전 크기로도 장치를 개발할 수 있어 실내외 구분 없이 설치와 활용이 용이하다는 장점을 가진다. 


- 제안하는 시스템의 여러가지 변종과 비교  
: http://news.jtbc.joins.com/article/article.aspx?news_id=NB10547358  
: 보행 중 스마트폰 사용을 막는 어플로, 키와 걷는 방식, 속도에 따라 움직임을 3단계로 등록한다. 걸으면 (금지 앱이) 작동하고 전철을 타면 작동하지 않는 어플이다. 이 어플리케이션도 스마트폰 보행 사고를 막기 위해 나온 어플이지만, 보행 중에 스마트폰을 사용하지 못한다는 거추장스러움을 사용자에게 유발할 수 있기에, 우리 시스템이 더 효율적으로 사용될 수 있다고 본다.  

---------------------------------------

##**4-7. 평가지표(metric)**
##**4-8. 독립변수, 종속변수**
##**4-9. 결과의 분석과 해석** 

**평가 지표**

1) **정확성을 보여주는 평가 지표**

- **비콘의 반경에 따른 메시지 전송 정확성**  
반경 4m 안의 비콘의 범위 안에서, 4m 안에 들어온 모든 사용자에게 알림 메시지가 전송되는지를 판단하는 실험

	- 독립 변수 (실험의 서로 다른 조건을 만들기 위한 변수)  : 비콘의 범위 (ex. 3.8m 일때, 3.9m 일때, 4.0m 일때, 4.1일때 등)  
	- 종속 변수 (실험을 통해 측정 가능한 것들) : 비콘의 데이터 전송 가능 범위
	- 결과 예측 : 한 조건당 20번

		|범위    | 정확도 |
		|:-------|:-------|
		| 3.8m   | 99.8%  |
		| 3.9m   | 99.8%  |
		| 4.0m   | 94.2%  |
		| 4.1m   | 13.2%  |

  	• 결과의 해석  

	 - **서로 다른 두 조건에 대한 측정 결과가 차이가 있는가?**
	 >정확성에 대한 실험의 조건들에 대해 범위 내에서는 차이가 거의 없지만 4m를 넘는 순간부터 메시지를 전송받을 확률이 매우 낮아진다.   

	 - **차이는 통계적으로 유의미한 것인가?**
	 > 비콘의 범위 안에서의 메시지 전송에 대한 정확성을 보여주는 자료로서 의미가 있다.  

	 - **차이를 만드는 이유는 무엇인가?**
 	 > 비콘의 범위인 4m를 넘어섰을 때 바로 메시지 전송이 중단되는 것이 아니라, 약하게나마 메시지가 전송되고 있기 때문에 False 메시지가 발생할 확률이 있다. 그래서 어느 범위까지 메시지 전송을 정확히 하는지 차이를 두어 실험을 하였다.  


- **사용자 설정에 따른 메시지 전송 정확성**  
(임의의 자동차도로에서, 사용자 설정에 따른 나이, 연령대의 사람들을 모아놓고 실험을 하여 위험도에 따른 등급 설정과 등급에 따른 	알림 메시지 전송이 정확한지를 판단하는 실험)    

	- 독립 변수 : 서로 다른 연령대의 사용자들   
	- 종속 변수 : 연령대 별 위험상황 등급에 따른 메시지 전송   
	- 결과 예측 : 연령대 별 인원 20명, 한 조건당 10번  
 > `전 연령대별 99.9%`  

  
  • 결과의 해석  
    
  - **서로 다른 두 조건에 대한 측정 결과가 차이가 있는가?** 
    > 차이가 없다.  
  	
   - **차이는 통계적으로 유의미한 것인가?**  
	 > 측정 결과에 차이가 없기 때문에 메시지가 모든 연령대에게 정확하게 전송되는 것으로서 의미가 있다.  
	 
 - **차이를 만드는 이유는 무엇인가?** 
  	>  이 실험에서 차이를 보인 이유는 사용자가 정보를 잘 못 입력했을 시 False 메시지가 전송되기 때문이다.   
  	>  사용자 연령대에 따라 차이를 만든 이유는 위험상황일 때 사용자들이 연령에 따라서 반응속도의 차이가 있기 때문이다. 

  
  
2) **신속성을 보여주는 평가 지표**

- **비콘의 반경에 따른 메시지 전송 신속성**  
  반경 4m 안의 비콘의 범위안에서, 모든 사용자에게 신속하게 알림 메시지를 전송할 수 있는가에 대한 실험

	- 독립 변수 : 비콘과 사람과의 거리 (ex. 3.8m 일때, 3.9m 일때, 4.0m 일때, 4.1일때 등)
	- 종속 변수 : 범위 안에서의 어플리케이션 응답 시간
	- 결과 예측 : 한 조건당 20번, 비콘 - 사용자 전송 평균 응답시간 : 0.5초 이내  

	|범위    |확률   |
	|:-------|:------|
	| 3.8m   | 99.8% |
	| 3.9m   | 99.8% |
	| 4.0m   | 94.2% |
	| 4.1m   | 3.2%  |

  • 결과의 해석		

	 - **서로 다른 두 조건에 대한 측정 결과가 차이가 있는가?**  
 > 신속성에 대한 실험의 조건들에 대해 범위 내에서는 차이가 거의 없지만 4m를 넘는 순간부터 평균 응답 시간 내에 메시지를 
	   전송 받을 확률이 매우 낮아진다.  

	 - **차이는 통계적으로 유의미한 것인가?**  
 	> 비콘의 범위 안에서의 메시지 전송에 대한 신속성을 보여주는 자료로서 의미가 있다.  

	 - **차이를 만드는 이유는 무엇인가?**  
 	> 비콘의 거리에 따른 신호의 세기가 약해짐에 따라 데이터 전송 속도가 떨어지기 때문이다.  
 
------------------------------------
====================================
##**소스**
![소스](http://postfiles12.naver.net/20151211_187/yhm1104_1449811589052GYLwa_PNG/KakaoTalk_20151202_123002856.png?type=w2)


-------------------------------------------

 - beacon.cpp
```cpp
/*
    Beacon은 속도와 메시지를 송수신을 한다.
*/
#include "Car.h"
#include "Message.h"


Message message;
double speed;

void receiveSpeed()	// 스피드건에서 차량의 속도를 받는 모듈
{
	speed = Speed values received by 'Speed Gun';
}

void sendSpeed()	// 서버로 메시지를 보내는 모듈
{
	it transmits the speed to the server.;
}
void receiveMessage() // 서버에서 메시지를 받는 모듈
{
	message = received by 'Server';
}
void sendMessage()  // 메시지를 전송하는 모듈
{
	사용자에게 메시지를 전송한다.
}


```
==============================================

-------------------------------------------

 - Car.h
```cpp
class Car {
private:
	double speed;
	int rate;
public:
	void setSpeed(double carSpeed);
	double getSpeed();
	void setRate(double limitSpeed);
	int getRate();
};


void Car::setSpeed(double carSpeed) // 측정된 차량 속도
{
	speed = carSpeed;
}

double Car::getSpeed() // 비콘으로 보낼 차량속도
{
	return speed;
}

void Car::setRate(double limitSpeed) 측정된 차량의 위험도 설정(해당 모듈은 서버에서 사용)
{
	if (limitSpeed < speed) // 현재 속도가 해당지역의 제한 속도를 넘은 경우
	{
        // 속도 차이를 가지고 위험도 설정
		if (speed - limitSpeed >= 20.0)
		{
			rate = 8;
		}
		else if(speed - limitSpeed >= 17.5)
		{
			rate = 7;
		}
		else if (speed - limitSpeed >= 15.0)
		{
			rate = 6;
		}
		else if (speed - limitSpeed >= 12.5)
		{
			rate = 5;
		}
		else if (speed - limitSpeed >= 10.0)
		{
			rate = 4;
		}
		else if (speed - limitSpeed  >= 7.5)
		{
			rate = 3;
		}
		else if (speed - limitSpeed >= 5)
		{
			rate = 2;
		}
		else
		{
			rate = 1;
		}
	}
	else
	{
		rate = 0;
	}
}

int Car::getRate() // 메시지에 위험도를 반환
{
	return rate;
}

```
==============================================

-------------------------------------------

 - Local.h
```cpp

enum class Weather { SUNNY, CLOUDY, RAINY, SNOWY }; // 날씨의 대한 상태

// 해당 class는 server에서 사용한다.
class Local {
private:
	Weather weather;
public:
	void setWeather(Weather weather);
	Weather getWeather();
};

void Local::setWeather(Weather weather) // 기상청에서 얻은 날씨를 해당 위치에 저장
{
	this->weather = weather;
}

Weather Local::getWeather() // 노면의 상태를 변경하기 위해 날씨를 반환
{
	return weather;
}

```
==============================================

-------------------------------------------

 - Message.h
```cpp
// class는 server와 beacon 그리고 user가 사용한다.
#include <iostream>
using namespace std;

class Message {
private:
	string message;
	int warning;
public:
	Message(int rate) // 메시지가 위험도를 받는 순간 생성이 된다.
	{
		message = "위험합니다. 주위를 살피세요.";
		warning = rate;
	}
	Message() {}
	int getWarning(); 
	string getMessage();
};

int Message::getWarning() // 사용자가 메시지의 위험도를 사용한다.
{
	return warning;
}

string Message::getMessage() // 사용자에게 알람이 발생된다고 판단 하면 해당 모듈을 호출하여 사용자에게 알람을 표시
{
	return message;
}



```
==============================================

-------------------------------------------

 - Road.h
```cpp
enum class Weather { SUNNY, CLOUDY, RAINY, SNOWY };

// 해당 class는 server에서 사용한다.
class Road {
private:
	int roadState;
	double limitSpeed;
public:
	void setRoadState(Weather weather);

	void setLimitSpeed();
	double getLimitSpeed();
};

void Road::setRoadState(Weather weather) // 해당 위치에 날씨에 따른 노면 상태를 측정
{
	if (Weather::SUNNY == weather)
	{
		roadState = 0;

	}
	else if (Weather::RAINY == weather)
	{
		roadState = 2;
	}
	else if (Weather::SNOWY == weather)
	{
		roadState = 3;
	}
	else if (Weather::CLOUDY == weather)
	{
		roadState = 1;
	}
}

void Road::setLimitSpeed() // 노면 상태에 따라 해당 도로의 위험 알림을 발생시키는 제한 속도를 설정한다.
{
	switch (roadState)	{
		case 0:
			limitSpeed = 60.0;
			break;
		case 1:
			limitSpeed = 55.0;
			break;
		case 2:
			limitSpeed = 50.0;
			break;
		case 3:
			limitSpeed = 40.0;
			break;
	}
}

double Road::getLimitSpeed() // 측정된 차량이 제한 속도를 넘어 갔는지 판독하기 위해 해당 지역의 제한 속도를 확인 하는 모듈
{
	return limitSpeed;
}



```
==============================================





-------------------------------------------

 - server.cpp
```cpp
#include "Car.h"
#include "Local.h"
#include "Message.h"
#include "Road.h"

#define N 10000 // 1만 군데 위치에 대해 서버가 처리해준다.

// 한 위치당 서버가 처리하는 모듈(해당 모듈은 쓰레드로 구성한다.)
void server()
{
	Local local;
	local.setWeather(기상청에서 얻은 해당 지역에 날씨); // 해당 지역의 날씨를 파악

	Road road;
	road.setRoadState(local.getWeather()); // 해당 지역의 날씨로 노면의 상태 변경
	road.setLimitSpeed(); // 저장된 노면 상태를 가지고 해당 지역에 제한 속도 설정
	

	double speed = 비콘에서 얻은 차량의 속도;

	Car car;
	car.setSpeed(speed); // 측정된 차량의 속도 설정
	car.setRate(road.getLimitSpeed()); // 측정된 차량의 위험도 설정

	Message message(car.getRate); // 보낼 메시지에 측정된 차량의 위험도를 저장

	Server is send a message to Beacon; // 비콘으로 메시지 전송
}


```
==============================================





-------------------------------------------

 - user.cpp
```cpp
/*
   사용자는 비콘에서 메시지를 받고 알림 여부를 판독한다.


#include "Message.h"


class User {
private:
    Message message; // 비콘에서 받은 메시지
	bool gender; // 성별
	int age; // 나이
	int warning; // 사용자 나이에 따른 위험도
public:
	void setMessage(Message message receive by beacon) // 비콘으로 부터 받은 메시지를 사용자에게 저장하는 모듈
	{
		this->message = message;
	}
	void setUserInfo(bool gneder, int age) // 사용자가 입력한 정보를 저장 하는 모듈
	{
		this->gender = gender;
		this->age = age;

		// true = man, false = women
        
        /*
           성별과 나이에 따른 위험도 설정
        */
		if (gender) 
		{
			if (age >= 60)
			{
				warning = 3;
			}
			else if (age >= 50)
			{
				warning = 4;
			}
			else if (age >= 50)
			{
				warning = 5;
			}
			else if (age >= 50)
			{
				warning = 6;
			}
			else if (age >= 50)
			{
				warning = 7;
			}
			else
			{
				warning = 8;
			}
		}
		else
		{
			if (age >= 60)
			{
				warning = 2;
			}
			else if (age >= 50)
			{
				warning = 3;
			}
			else if (age >= 50)
			{
				warning = 4;
			}
			else if (age >= 50)
			{
				warning = 5;
			}
			else if (age >= 50)
			{
				warning = 6;
			}
			else
			{
				warning = 7;
			}
		}
	}

	void alram() // 알람 메시지 모듈
	{
		if (warning <= message.getWarning) // 사용자가 설정된 위험도와 메시지에서 얻은 위험도를 비교
		{
			Display(message.getMessage); // 조건이 참인 경우 메시지를 출력
		}
	}
};
```
==============================================
----------------------------------------------

##**상태 다이어그램**
- 차량 속도에 따른 위험도의 변화
![모듈1](http://postfiles8.naver.net/20151211_7/yhm1104_1449811593965OglS1_JPEG/KakaoTalk_20151203_130639684.jpg?type=w2)  
=====================================

- 날씨에 따른 노면 상태 변화
![모듈2](http://postfiles10.naver.net/20151211_73/yhm1104_1449811598581iGwmf_JPEG/KakaoTalk_20151203_130639889.jpg?type=w2)  
=====================================

- 노면 상태에 따른 차량의 제한속도 변화
![모듈3](http://postfiles14.naver.net/20151211_109/yhm1104_1449811602657HnpJG_JPEG/KakaoTalk_20151203_130640121.jpg?type=w2)  
=====================================


