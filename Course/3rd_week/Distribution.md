# 확률 분포

> 데이터의 모습이 어떻게 나타나는지 확인하고,
다양한 분포들간의 관계를 분석하기 위한 방법을 알아본다.
> 

## 확률 변수  Random Variable

---

![image.png](image.png)

- 이 그림은 어떤 확률 변수일까?
    
    ‘동전을 3번 던졌을 때 앞면이 나온 횟수’
    

<aside>
💡

**확률 변수란?**

---

- **함수**
    - feature
- Event → Random Variable → Real Number
- 현실에서 발생하는 **사건**을 **실수**로 매핑해주는 함수
    - ‘키’, ‘나이’, ‘성별’
</aside>

<aside>
💡

**이산 확률 변수  Discrete Random Variable**

---

- 확률 변수 X의 값이 범위 내에서 불연속적인 값을 가진다.
- 유한, 셀 수 있는 무한, 불연속
- 시그마, 나누기
- ex. 주사위 숫자, 제출한 문제
</aside>

<aside>
💡

**연속 확률 변수  Continuous Random Variable**

---

- 확률 변수의 값이 연속적인 범위의 값을 가진다.
- 무한
- 적분, 미분
- ex. 키, 시간, 온도
</aside>

<aside>
💡

**다음과 같은 표본 공간이 존재한다.**

</aside>

![image.png](image%201.png)

<aside>
💡

**동전을 3번 던졌을 때, 앞면이 0번 초과, 2번 이하로 나올 확률은?**

</aside>

![image.png](image%202.png)

![image.png](image%203.png)

![image.png](image%204.png)

## 이산 확률 분포 & 연속 확률 분포  Probability Distribution

---

<aside>
💡

**확률 분포**

---

- 분포란, 일정한 범위에 흩어져 퍼져 있는 것
- **확률 분포는, 확률 변수에 따라 확률이 어떻게 흩어져 있는지를 표현한다.**
</aside>

![image.png](image%205.png)

### 확률 질량 함수  Probability Mass Function

---

![image.png](image%206.png)

<aside>
💡

**이산 확률 변수의 확률 질량 함수**

---

![image.png](image%207.png)

</aside>

<aside>
💡

**확률 질량 함수의 성질**

---

![image.png](image%208.png)

</aside>

### 누적 분포 함수  Cumulative Distribution Function

---

<aside>
💡

**누적 분포 함수 - 범위의 개념**

---

![image.png](image%209.png)

</aside>

![image.png](image%2010.png)

![image.png](image%2011.png)

<aside>
💡

**P(1 < X ≤ 3)) = ???**

---

F(x)가 누적 분포 함수라면,

P(a < X ≤) = F(b) - F(a) 이다.

</aside>

### 확률 밀도 함수  Probability Density Function

---

<aside>
💡

**확률 밀도 함수**

---

![image.png](image%2012.png)

</aside>

![image.png](image%2013.png)

<aside>
💡

**확률 질량 함수에서 시그마를 이용했던 것과 달리 확률 밀도 함수에서는 적분을 이용**

</aside>

### 연속 확률 변수의 누적 분포 함수

---

<aside>
💡

**연속 확률 변수의 누적 분포 함수**

---

![image.png](image%2014.png)

</aside>

![image.png](image%2015.png)

<aside>
💡

**질량/밀도 함수를 시그마/적분 ⇒ 누적 분포 함수**

**누적 분포 함수를 나누기/미분 ⇒ 질량/밀도 함수**

</aside>

<aside>
💡

**이외에 알아둬야 할 것**

---

- **결합 확률 분포**
- **주변 확률 분포**
- 조건부 분포
</aside>

<aside>
💡

**꼭 알아둬야 할 것** 

---

- **기댓값 -** 평균으로서 기대할 수 있는 값
- **분산과 표준편차 -** 확률 변수가 평균으로부터 떨어진 정도를 표현한 값
- **공분산 -** 확률 변수 X와 Y에 대해 X가 변할 때 Y가 변하는 정도
- **상관계수 -** 측정 단위 영향 x
</aside>

<aside>
💡

**확률과 기댓값의 관계**

---

- 마르코프 부등식
- 체비쇼프 부등식
</aside>

## 다양한 확률 분포

---

- 실제 세상의 데이터는 특정한 분포를 가지게 된다.
- 다양한 Feature - 확률 변수 - 데이터의 분포가 어떻게 나타나는지 살펴보자.

## 베르누이 분포  Bernoulli Distribution

---

<aside>
💡

**베르누이 분포**

---

- 시행의 결과가 **성공** 또는 **실패** 중 하나로 나타난다.
- 성공일 확률을 p, 실패할 확률을 q = 1 - p라고 하자.
- 그 결과가 성공이면 확률 변수 X가 1을 갖고, 실패하면 0을 가진다.
- 이 때의 확률 변수 X를 베르누이 확률변수라 한다.
</aside>

### 확률 질량 함수

---

![image.png](image%2016.png)

### 모멘트

---

![image.png](image%2017.png)

### 예시

---

![구글의 동전 던지기](image%2018.png)

구글의 동전 던지기

![COVID-19 자가 검사 키트](VnYEMju8AaoAwm9Tlh.jpg)

COVID-19 자가 검사 키트

### 분포

---

![ComputeBernoulliDistributionPdfExample_01.png](ComputeBernoulliDistributionPdfExample_01.png)

## 이항 분포  Binomial Distribution

---

<aside>
💡

**이항 분포**

---

- **베르누이 시행**을 n번 반복한다.
    - 시행의 결과가 성공과 실패
- 성공이 나타난 횟수를 확률 변수 X라고 하자
- 성공이 나오는 횟수를 확률변수 X라고 했을 때, 이 확률 변수를 **이항 확률 변수**라 한다.
</aside>

<aside>
💡

성공 확률이 p인 베르누이 시행이 n번 반복되었을 때,
그리고 성공 횟수를 확률 변수 X라 할 때,

**X를 이항 확률 변수**라고 한다.

</aside>

<aside>
💡

- 베르누이 분포는 이항 분포의 특수한 경우 (표본 데이터가 하나)
- 베르누이 시행을 n회 시행할 때, 각 시행은 서로 독립이다.
</aside>

### 확률 질량 함수

---

![image.png](image%2019.png)

### 모멘트

---

![image.png](image%2020.png)

### 예시

---

![download.jpg](download.jpg)

![image.png](image%2021.png)

### 분포

---

![image.png](image%2022.png)

## 다항 분포(카테고리 분포)  Multinomial Distribution

---

<aside>
💡

**다항 분포**

---

- 베르누이 시행은 실행의 결과가 성공과 실패 두 가지 뿐이었다.
- 시행의 결과가 세 가지, 네 가지, 또는 그 이상의 경우,
즉, 발생 결과가 3개 이상일 때에는 **다항 분포**를 적용한다.
</aside>

### 확률 질량 함수

---

![image.png](image%2023.png)

### 모멘트

---

![image.png](image%2024.png)

### 예시

---

![image.png](image%2025.png)

### 분포

---

![08.03 카테고리분포와 다항분포_26_0.png](08.03_%25EC%25B9%25B4%25ED%2585%258C%25EA%25B3%25A0%25EB%25A6%25AC%25EB%25B6%2584%25ED%258F%25AC%25EC%2599%2580_%25EB%258B%25A4%25ED%2595%25AD%25EB%25B6%2584%25ED%258F%25AC_26_0.png)

## 초기하 분포  Hypergeometric Distribution

---

<aside>
💡

**상자 안의 공**

---

상자 안에는 10개의 공이 있다. 이 중 6개는 흰 공, 4개는 검은 공이다.

당신은 5개의 공을 꺼냈다.

이 때, 흰 공이 3개일 확률은?

</aside>

<aside>
💡

**초기하 분포**

---

- k개의 성공과 N-k개의 실패로 구성된 크기가 N인 유한 모집단이 있다고 하자.
- **크기가 n인 확률 표본**을 취하고, 성공의 개수를 X라고 하면,
이 X를 **초기하 확률 변수**라고 한다.
</aside>

### 확률 질량 함수

---

![image.png](image%2026.png)

### 모멘트

---

![image.png](image%2027.png)

### 예시

---

![image.png](image%2028.png)

![[https://blog.naver.com/mykepzzang/220607187232](https://blog.naver.com/mykepzzang/220607187232)](download%201.jpg)

[https://blog.naver.com/mykepzzang/220607187232](https://blog.naver.com/mykepzzang/220607187232)

### 분포

---

![hypergeometricdistribution_3_def.png](hypergeometricdistribution_3_def.png)

## 기하 분포  Geometric Distribution

---

<aside>
💡

**즐거운 날**

---

매주 로또를 사던 어느 날, 더 이상 이런 의미 없는 짓을 하지 않기로 다짐한다.

그래도 마지막 한 번만 더, 로또를 사게 되었는데… 당첨이 되어버렸다.

매주 로또 당첨에 실패하다가, 이번 주에 당첨될 확률은 얼마나 될까?

</aside>

<aside>
💡

**기하 분포**

---

- 성공일 확률이 p인 베르누이 시행을 독립적으로 반복한다.
- 처음 성공할 때까지의 시행 횟수를 확률 변수 X라고 할 때,
이 **X를 기하 확률 변수**라고 한다.
</aside>

<aside>
💡

**처음 성공이 나올 때 까지 얼만큼 시도했는지가 중요하다.**

</aside>

### 확률 질량 함수

---

![image.png](image%2029.png)

### 모멘트

---

![image.png](image%2030.png)

### 예시

---

![image.png](image%2031.png)

### 분포

---

![img1.daumcdn.png](img1.daumcdn.png)

## 음이항 분포  Negative Binomial Distribution

---

<aside>
💡

**Best of 7**

---

A팀과 B팀이 우승을 놓고 다투게 되었다.

A팀과 B팀의 상대 전적을 살펴보니, A팀과 B팀에게 승리할 확률이 0.582 이다.

이 시리즈는 7경기 중 4 경기를 먼저 승리한 팀이 우승하게 된다.

이 때, A팀이 6번째 경기에서 우승을 확정 지을 확률은?

</aside>

<aside>
💡

**음이항 분포**

---

- 성공 확률이 p인 베르누이 시행을 독립적으로 반복하자.
- k 번째 성공이 나올 때 까지 시행 횟수를 확률변수 X라고 할 때,
이 확률 변수 X를 **음이항 확률 변수**라고 한다.
</aside>

### 확률 질량 함수

---

![image.png](image%2032.png)

### 모멘트

---

![image.png](image%2033.png)

### 예시

---

![image.png](image%2034.png)

![image.png](image%2035.png)

### 분포

---

![c1755c80988c619a6c0e40d903d248de.png](c1755c80988c619a6c0e40d903d248de.png)

## 음초기하 분포  Negative Hypergeometric Distribution

---

<aside>
💡

**볶음밥**

---

아까와 같이, 상자에 흰 공이 6개, 검은 공이 4개 들어있다고 하자.

나는 흰 공을 처음 뽑을려면, 몇 개의 검은 공을 뽑게 될까?

</aside>

<aside>
💡

**음초기하 분포**

---

- k개의 성공과 N-k개의 실패로 구성된 크기가 N인 유한 모집단이 있다고 하자.
- 처음 성공하기 전까지 실패의 개수를 X라고 하면,
이 X를 음**초기하 확률 변수**라고 한다.
</aside>

### 확률 질량 함수

---

![image.png](image%2036.png)

### 모멘트

---

![image.png](image%2037.png)

### 예시

---

```
52장의 플레잉 카드를 고루 섞고, 한 장씩 나누어준다.
이 때, 에이서 카드가 나오면 성공이라고 하자.

첫 번째 에이스를 뽑기 위해서는,

E(X) = (52-4) / (4+1) = 9.6

평균 9.6자의 카드를 먼저 뽑아야 한다.
```

## 관계성

---

|  | **복원 추출** | **비복원 추출** |
| --- | --- | --- |
| **시행 횟수 고정** | 이항 분포 | 초기하 분포 |
| **성공 횟수 고정** | 음이항 분포 | 음초기하 분포 |

<aside>
💡

**이항 분포**

---

- 시험 문제 25문제를 찍어서 다 맞힐 확률
- 시행 횟수가 고정되어 있다.
- 각 시행이 영향을 주지 않아.
</aside>

<aside>
💡

**초기하 분포**

---

- 1000개의 제품 중 20개를 뽑는 것
- 20이라는 시행 횟수가 정해져있다.
- 공을 뽑으면 다시 상자에 넣지 않아.
</aside>

<aside>
💡

**음이항 분포**

---

- BO7에서 4번 먼저 승리
- 시행 횟수가 아닌 성공 횟수를 정했다.
</aside>

<aside>
💡

**음초기하 분포**

---

- 공 뽑기, 카드 뽑기
- 뽑으면 다시 넣지 않는다.
</aside>

<aside>
💡

**비복원 추출은 앙상블에 또 나와요.**

</aside>

## 포아송 분포  Poisson Distribution

---

<aside>
💡

**모수 - 모집단의 특성을 나타내는 수치 (lambda λ)**

---

- **단위 시간, 또는 단위 공간에서 평균 발생 횟수가 λ인 사건의 발생 횟수의 분포**
    - 한 시간 동안 은행에 다녀간 고객의 수
    - 한 시간 동안 사무실에 걸려온 전화의 수
    - 어떤 책의 한 페이지에 존재하는 오타의 수
</aside>

<aside>
💡

**포아송 분포**

---

- **단위 시간, 단위 공간에 어떤 사건이 몇 번 발생할 것인가를 표현하는 분포**
</aside>

<aside>
💡

포아송 과정

- 어떤 사건의 발생 횟수가 포아송 분포를 따르는 확률 과정

확률 과정

- 시간과 관련된 확률 적인 성격을 갖는 것

---

**⇒ 시간에 따라 확률이 변한다.**

</aside>

<aside>
💡

**전제 조건**

---

- **독립성**
    - 어떤 단위 시간 또는 단위 공간에서 발생한 결과는 중복되지 않은 다른 시간이나 공간에서 발생한 결과와 서로 독립이다.
    - ex. 후 1시에서 2시 사이에 응급실로 들어오는 환자 수와 오후 2시에서 3시 사이에 들어오는 환자 수는 서로 독립이다. ⇒ **사건 발생의 독립성**
    - 오후 1시에서 3시까지의 2시간을 [1시-2시]와 [2시-3시] 두 개의 비중첩 구간으로 나눈다면, 각 구간에서 발생하는 환자 수는 서로 독립적이다. ⇒ **비중첩 구간의 독립성**
- **일정성**
    - 어떤 단위 시간 또는 단위 공간에서 발생한 확률은 그 시간의 크기, 혹은 공간의 크기에 비례하고, 외부의 영향을 받지 않는다.
    - 즉 단위 시간이나 공간에서 발생한 평균 발생 횟수는 일정하다.
    - ex. 만약 어떤 사건이 1분에 평균 2번 발생한다면, 3분 동안에는 평균 6번 발생
- **비집락성**
    - 매우 짧은 시간이나 매우 작은 공간에 두 개 이상의 결과가 동시에 발생할 확률은 0이다.
    - ex. 같은 시간에 같은 지점에서 같은 사고가 두 번 발생할 확률은 무시해도 좋다.
</aside>

### 확률 질량 함수

---

![image.png](image%2038.png)

### 모멘트

---

![image.png](image%2039.png)

![image.png](image%2040.png)

### 예시

---

![image.png](image%2041.png)

![image.png](image%2042.png)

### 분포

---

![SE-ac56c406-dc74-424a-899d-e78438d3e297.png](SE-ac56c406-dc74-424a-899d-e78438d3e297.png)

### 베이즈 통계학

---

![image.png](image%2043.png)

## 균일 분포  Uniform Distribution

---

<aside>
💡

**버스가 온다**

---

10시 10분부터 10시 20분까지,
언제 버스가 가장 올 확률이 높을까?

</aside>

<aside>
💡

**균일 분포**

---

- 모든 확률 변수에 대해 균일한 확률을 갖는다.
- 확률 변수 X가 폐구간 [a, b]내에 모든 영역에서 일정한 확률을 가질 때,
이 확률 변수 X를 **균일 확률 변수**라고 한다.
- **균일 분포는 이산 확률 변수에서도 가능하다.**
</aside>

### 확률 밀도 함수

---

![image.png](image%2044.png)

### 모멘트

---

![image.png](image%2045.png)

### 예시

---

![image.png](image%2046.png)

### 분포

---

![image.png](image%2047.png)

## 지수 분포  Exponential Distribution

---

<aside>
💡

**감마 분포의 특수한 경우**

---

감마 분포의 **α = 1** 일 때

</aside>

<aside>
💡

**지수 분포**

---

- 단위 구간 동안 발생 횟수의 기댓값이 1/β인 사건이 처음 발생할때까지 대기시간의 분포
- 어떤 사건이 처음으로 발생하기까지 걸린 **시간**에 대한 분포
- 즉, 포아송 과정에서 어떤 사건이 처음으로 발생하기까지의 시간
</aside>

### 확률 밀도 함수

---

![image.png](image%2048.png)

### 모멘트

---

![image.png](image%2049.png)

![image.png](image%2050.png)

### 예시

---

![image.png](image%2051.png)

### 분포

---

![image.png](image%2052.png)

<aside>
💡

**시간이 흐를 수록 생명체가 살아있는 확률이 감소하고,**

**전자 제품이 고장나지 않을 확률이 작아지는 것**

</aside>

<aside>
💡

**지수 분포와 생명체의 생존 확률**

---

**지수 분포**는 특정 사건이 일정한 비율로 발생하는 상황에서, 사건이 발생할 때까지의 시간 분포를 모델링합니다. 이는 **메모리리스(memoryless)** 성질을 가지고 있어서, 현재 시점에서 앞으로의 생존 시간은 과거와 무관하게 동일한 분포를 따릅니다. 이 성질은 생명체의 생존 분석에 자주 사용됩니다.

</aside>

<aside>
💡

**메모리리스(무기억성)**

---

어떤 기계가 처음 만들어져서 사용되기 시작한 뒤 s시간 이내에 고장날 확률과
그 기계가 계속 사용 되다가 s시간 이내에 고장날 확률은 동일하다는 말이다.

마치 기계가 이 전 t시간 동안 사용되었다는 것을 기억하지 못하는 것과 같다고 해서 이를 무
기억(Memoryless) 성질이라 한다.

**어떤 사건이 발생할 때까지 걸린 시간을 지수분포가 설명할 수 있는 이유는 지수분포의 무기억 성질 때문이다.**

</aside>

## 감마 분포  Gamma Distribution

---

<aside>
💡

**감마 분포**

---

- 감마 함수로부터 유도된 분포
- 지수 분포의 일반화
- **α 번째 사건이 일어날 때까지 걸리는 시간에 대한 연속 확률 분포**
- 포아송 과정에서 어떤 사건이 α 번째 발생하기까지 걸린 **시간**에 대한 분포
- β는 포아송 분포의 모수 λ와 비슷한 역할을 한다.
- α는 형태 모수, β는 척도 모수
</aside>

### 확률 밀도 함수

---

![image.png](image%2053.png)

![image.png](image%2054.png)

### 모멘트

---

![image.png](image%2055.png)

- 기댓값과 분산은 **적률 생성 함수**를 통해 유도한다.

### 예시

---

![image.png](image%2056.png)

### 분포

---

![image.png](image%2057.png)

## 베타 분포  Beta Distribution

---

<aside>
💡

**베타분포**

---

- 이항 계수를 실수 범위까지 확장한 베타 함수의 분포
</aside>

### 확률 밀도 함수

---

![image.png](image%2058.png)

### 모멘트

---

![image.png](image%2059.png)

### 예시

---

![image.png](image%2060.png)

### 분포

---

![image.png](image%2061.png)

## 정규 분포(가우스 분포)  Normal Distribution

---

<aside>
💡

**이 세상에서 가장 중요한 분포**

</aside>

<aside>
💡

**자연계를 설명하는 분포**

</aside>

### 확률 밀도 함수

---

![image.png](image%2062.png)

### 모멘트

---

![image.png](image%2063.png)

![image.png](image%2064.png)

### 분포

---

![평균을 중심으로 좌우 대칭인 종 모양.
분산이 커질수록 옆으로 늘어진다.](image%2065.png)

평균을 중심으로 좌우 대칭인 종 모양.
분산이 커질수록 옆으로 늘어진다.

![평균이 다른 경우](image%2066.png)

평균이 다른 경우

![분산이 다른 경우
평균에 더 밀집한 분포가 더 고른 정규 곡선](image%2067.png)

분산이 다른 경우
평균에 더 밀집한 분포가 더 고른 정규 곡선

### 세상은 정말로 정규 분포?

---

- 오른쪽 꼬리 분포
- 왼쪽 꼬리 분포

<aside>
💡

**세상은 정규 분포 형태로 편성되어있지 않다.**

---

다만, 어떤 모집단에서 표본을 추출했을 경우에 **모집단이 어떤 모양을 하고있던지 간에,
결과는 정규 분포를 따른다**.

따라서 이론적으로 통계적으로 편향되지 않은, 신뢰성있고 적절한 표본선출만 한다면 **사회전체의 정규분포**를 추출할 수 있게된다.

모든 사회실험, 과학에서 모집단에서 특정한 **표본**을 뽑아 모집단의 성격을 탐구하는 방식이 사용될 수 밖에 없으므로 모든 곳에 정규분포가 쓰이는 것이다.

</aside>

## 표준 정규 분포(z-분포)  Standard Normal Distribution

---

<aside>
💡

**표준화된 정규 분포** 

</aside>

![image.png](image%2068.png)

<aside>
💡

A와 B 두 정규 분포가 있고, 구하려는 확률의 범위는 x1 < X < x2 로 같다.

그러나 A와 B에서의 확률은 분명히 다르다.

A와 B의 확률을 비교하고자 한다면, 평균과 표준 편차를 일치시켜야 한다.

</aside>

<aside>
💡

**표준화 (정규화)**

---

![image.png](image%2069.png)

데이터에서 평균을 빼고 표준 편차를 나눈다.

</aside>

<aside>
💡

**표준 정규 분포**

---

- 평균 0, 표준 편차 1을 가지는 정규 분포를 **표준 정규 분포**라고 한다.
</aside>

### 확률 밀도 함수

---

![image.png](image%2070.png)

### 모멘트

---

![image.png](image%2071.png)

### 예시

---

![image.png](image%2072.png)

### 분포

---

![정규화](image%2073.png)

정규화

![누적 분포 함수](image%2074.png)

누적 분포 함수

## 독립 항등 분포  independent and identically distributed

---

<aside>
💡

**Independent and identically distributed**

---

- **확률 변수나 데이터 포인트들이 서로 독립적이며 동일한 확률 분포를 따른다는 가정**
- iid 조건에서 추출한 표본을 **확률 표본**이라고 한다.
</aside>

<aside>
💡

**Independent  독립적**

---

- 각각의 데이터나 확률 변수가 다른 것들과 상관 없이 독립적으로 발생한다는 의미
- 즉, 하나의 데이터 포인트나 확률 변수의 값이 다른 데이터나 변수에 영향을 미치지 않는다고 가정한다.
</aside>

<aside>
💡

**Identically Distributed  동일한 분포를 따름**

---

- 모든 데이터 포인트나 확률 변수가 동일한 확률 분포를 따른다는 의미입
- 이는 데이터들이 동일한 모집단에서 추출되었거나 같은 확률 분포를 가지는 형태로 모델링될 수 있다는 가정을 의미합니다.
</aside>

<aside>
💡

**예시**

---

- 동전을 여러 번 던질 때, 각 시행이 독립적이고, 
앞면이 나올 확률이 같아서 동일한 분포를 따르므로, 
iid이다
</aside>

## 중심 극한 정리  Central Limit Theorem

---

<aside>
💡

**중심 극한 정리**

---

**무작위로 추출된 표본의 크기가 커질수록,
표본 평균의 분포는 모집단의 분포 모양과는 관계없이 정규 분포에 가까워진다.**

---

**동일한 확률 분포를 가진 독립 확률 변수 n개의 평균의 분포는 n이 적당히 크다면 정규 분포에 가까워진다.**

</aside>

![image.png](image%2075.png)

![Clt_in_action.gif](Clt_in_action.gif)

### 3가지 가정

---

<aside>
💡

**왜 iid가 필요한데?**

---

- **독립성 유지**
    - 독립적인 표본이 모여야 각 표본의 기여가 고유하고, 하나의 표본이 다른 표본의 결과에 영향을 주지 않게 된다. 독립성이 유지될 때, 전체의 합이나 평균이 점점 더 정규분포에 가까워지는 과정을 기대할 수 있다.
- **분포의 일관성**
    - 동일한 분포를 따라야 각 표본의 기댓값과 분산이 일정하게 유지되며, 이로 인해 많은 표본이 합쳐졌을 때 특정한 정규분포의 형태로 수렴할 수 있습니다.
</aside>

<aside>
💡

**계산된 분산은 유한해야 한다.**

---

ex. 주사위의 가능한 결과값은 6개이다.

</aside>

<aside>
💡

[https://www.youtube.com/watch?v=SoKjCUcDBf0&t=266s](https://www.youtube.com/watch?v=SoKjCUcDBf0&t=266s)

</aside>

### 활용

---

<aside>
💡

**표본 평균을 통한 추론**

---

- **상황**: 데이터 분석을 할 때, 모집단의 평균을 알고 싶지만, 데이터를 모두 수집할 수 없을 때가 많습니다. 예를 들어, 한 도시의 평균 소득을 알고자 할 때, 모든 시민의 소득을 조사하기보다는 **일부 표본만** 조사하여 전체 인구의 평균 소득을 추정하게 됩니다.
- **중심극한정리의 적용**: 도시 전체 인구의 소득이 어떤 분포를 따르든, **충분히 큰 표본**을 여러 번 추출한 후 그 표본평균을 구하면, 그 평균들은 정규분포에 가까워집니다. 따라서 표본평균을 이용해 모집단의 평균을 추정할 수 있고, **정규분포의 성질**을 이용해 신뢰구간을 설정할 수 있습니다.
- **결과**: CLT를 기반으로 도시 전체의 평균 소득에 대한 정확한 추정을 할 수 있으며, 이 추정을 통해 도시의 정책이나 재정 계획을 세울 수 있습니다.
</aside>

<aside>
💡

**모델 평가**

---

- **상황**: 머신러닝 모델의 성능을 평가할 때, 보통 **교차 검증**(Cross-Validation)을 사용합니다. 교차 검증에서는 데이터를 여러 번 나누어 모델을 훈련시키고 평가합니다. 이때 각각의 검증 세트에서 나온 모델의 성능 지표(예: 정확도, 정밀도 등)가 각기 다를 수 있습니다.
- **중심극한정리의 적용**: 만약 각 검증에서 얻은 성능 지표가 독립적이고 동일한 분포에서 추출되었다고 가정할 수 있다면, 그 성능 지표들의 **평균**은 정규분포에 가까워집니다. 이를 통해 성능 평균에 대한 신뢰구간을 구하고, 모델의 **성능 안정성**을 평가할 수 있습니다.
- **결과**: 교차 검증 결과에 기반하여 모델의 성능이 통계적으로 유의미한지 판단할 수 있고, 다른 모델들과의 비교도 더 정확하게 할 수 있습니다.
</aside>

<aside>
💡

**A/B 테스트**

---

- **상황**: A/B 테스트는 웹사이트에서 새로운 디자인이나 기능의 효과를 테스트할 때 많이 사용됩니다. 예를 들어, 한 전자상거래 사이트에서 새로운 구매 버튼 디자인을 적용했을 때 **전환율**(구매로 이어지는 방문자 비율)이 얼마나 증가했는지 알고 싶다고 가정합시다.
- **중심극한정리의 적용**: 각 방문자의 구매 여부는 이항분포를 따를 수 있습니다(구매 또는 비구매). A/B 테스트 결과에서 새로운 디자인을 적용한 그룹과 기존 디자인을 사용한 그룹의 **표본평균 전환율**을 구하면, 그 차이가 정규분포에 가까워집니다. 이때 중심극한정리를 사용해 **두 그룹 간의 전환율 차이가 우연에 의한 것인지 아닌지**를 통계적으로 판단할 수 있습니다.
- **결과**: CLT를 통해 전환율 차이에 대한 **통계적 유의성**을 검정할 수 있으며, 이는 A/B 테스트의 결과를 더 신뢰할 수 있게 만듭니다.
</aside>

### 코드

---

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# 샘플 개수와 표본 크기 설정
num_samples = 10000
sample_sizes = [1, 30, 100, 1000]

# 그래프 그리기 함수
def plot_clt_distribution(distribution, dist_name):
    plt.figure(figsize=(12, 8))
    
    for i, sample_size in enumerate(sample_sizes):
        plt.subplot(2, 2, i+1)
        
        # 표본 생성 후 표본 평균 계산
        sample_means = [np.mean(distribution(size=sample_size)) for _ in range(num_samples)]
        
        # 히스토그램으로 분포 시각화
        sns.histplot(sample_means, bins=30, kde=True, color='skyblue', stat='density')
        plt.title(f'{dist_name} Distribution - Sample Size: {sample_size}')
        plt.xlabel('Sample Mean')
        plt.ylabel('Density')

    plt.tight_layout()
    plt.show()
    

# 이항 분포(Binomial Distribution)
n_binom = 10  # 시도 횟수
p_binom = 0.5  # 성공 확률

plot_clt_distribution(lambda size: np.random.binomial(n=n_binom, p=p_binom, size=size), 'Binomial')

# 포아송 분포(Poisson Distribution)
lambda_poisson = 3  # 평균 발생 횟수

plot_clt_distribution(lambda size: np.random.poisson(lam=lambda_poisson, size=size), 'Poisson')
```

## 카이 제곱 분포  Chi-Squared Distribution

---

[https://www.youtube.com/watch?v=Iffx42lmQD4](https://www.youtube.com/watch?v=Iffx42lmQD4)

<aside>
💡

**카이 제곱 분포**

---

- k개의 서로 독립적인 표준 정규 확률 변수를 각각 제곱한 다음 합해서 얻어지는 분포
- 감마 분포의 특수한 형태
    
    ![image.png](image%2076.png)
    
- k차원 확률벡터 y ~ N(0, I)에 대해
    
    ![image.png](image%2077.png)
    
</aside>

### 확률 밀도 함수

---

![image.png](image%2078.png)

### 모멘트

---

![image.png](image%2079.png)

### 예시

---

<aside>
💡

**범주형 자료 분석**

---

- 적합도 검정
    - 주사위를 던졌을 때 각 면이 동일한 확률로 나오는지 확인하고 싶다면, 카이 제곱 적합도 검정을 사용
- 동질성 검정
- 독립성 검정
    - **성별**과 **영화 장르 선호도**가 독립적인지 여부를 확인하려고 할 때 카이 제곱 독립성 검정을 사용
    - 카이 제곱 분포는 기대 빈도와 관측 빈도의 차이를 기반으로 하므로, 그 차이가 클수록 두 변수는 독립적이지 않다고 판단할 수 있다.
</aside>

<aside>
💡

**상관 관계나 인과 관계를 판별하고자 하는 원인의 독립 변수가
”완벽하게 서로 다른 질적 자료” 일 때 활용**

</aside>

<aside>
💡

**카이-제곱 분포를 σ^2을 구할 때 사용하여 모분산 검정, 적합도 검정, 독립성/동질성 검정 등에 사용한다**

- 주식 시장의 변동성을 분석할 때, 과거 주가 데이터를 이용해 표본 분산을 계산하고 이를 통해 모집단의 분산을 추정할 수 있다.
</aside>

<aside>
💡

**선거 여론조사에서 남성/여성, 연령대별(18-29세, 30대, 40대, 50대, 60대, 70대 이상)별 지지율 등을 알아볼 때 쓴다**

</aside>

<aside>
💡

**남성과 여성, 성별로 보수 성향과 진보 성향의 비율에 유의한 차이가 있는가**

</aside>

### 분포

---

![EMU1GCu5aA5y2hYbrN22GPLQ4-oosFKd3ST7848vVzoSh3z3tyjyEHB-Ik8hkhsXihMs27JUtAXAHRQNmpR6_uyaTnUFApQbltNPyYAS9rakF3piGZwXTvI5lOjxOhSQDBcMZbVlCB3pro4BJnOdZA.webp](EMU1GCu5aA5y2hYbrN22GPLQ4-oosFKd3ST7848vVzoSh3z3tyjyEHB-Ik8hkhsXihMs27JUtAXAHRQNmpR6_uyaTnUFApQbltNPyYAS9rakF3piGZwXTvI5lOjxOhSQDBcMZbVlCB3pro4BJnOdZA.webp)

## t 분포  Student’s t-Distribution

---

[https://www.youtube.com/watch?v=v8QBYFNoC-U](https://www.youtube.com/watch?v=v8QBYFNoC-U)

<aside>
💡

**t 분포**

---

- 독립적인 표준정규분포 확률 변수 X와 자유도가 k인 카이 제곱 분포 확률 변수 Y에 대해$X/\sqrt{Y/k}$가 가지는 분포
</aside>

### 확률 밀도 함수

---

![image.png](image%2080.png)

![image.png](image%2081.png)

### 예시

---

<aside>
💡

**독립 표본 t 검정**

---

- 등분산
- 이분산
- F-검정으로 등분산인지 이분산인지 검증해봐서 F-검정의 p-value값이 0.05보다 작으면 이분산, 크면 등분산이다
- 두 반의 성적 평균 차이가 통계적으로 유의한 차이가 있는가?
</aside>

<aside>
💡

**대응 표본 t 검정**

---

- 두 집단 간의 차이를 비교하는 독립 표본 t-test와는 달리, paired t-test는 같은 집단의 전후 차이를 비교한다.
- 특정 수업을 들은 전후의 성적 차이나, 약물 복용 후 효과 차이와 같은 것
</aside>

### 분포

---

![0zt6oR30a59r1yZ0leChss6vWPhDzxaCBfpDefEbgLpV-JPRn0hptKv-oNvCwFi5H4pBDA_cCZW1hCX_MklhNBg7067g-C2prxXvvRe_xkUt9s-STbOXwUFYbrCe8J3xV0R-su5JYHAgXe-LCyWrDg.webp](0zt6oR30a59r1yZ0leChss6vWPhDzxaCBfpDefEbgLpV-JPRn0hptKv-oNvCwFi5H4pBDA_cCZW1hCX_MklhNBg7067g-C2prxXvvRe_xkUt9s-STbOXwUFYbrCe8J3xV0R-su5JYHAgXe-LCyWrDg.webp)

## F 분포  Snedecor’s F-Distribution

---

[https://www.youtube.com/watch?v=xmDs5s-1beo](https://www.youtube.com/watch?v=xmDs5s-1beo)

<aside>
💡

**F 분포**

---

- 정규 분포를 이루는 모집단에서 독립적으로 추출한 표본들의 분산 비율이 나타내는 연속 확률 분포입니다.
- 두 가지 이상의 표본집단의 분산을 비교하거나 모집단의 분산을 추정
- **2개 이상의 표본 평균들이 동일한 모평균을 가진 집단에서 추출되었는지,
아니면 서로 다른 모집단에서 추출된 것인지 판단하기 위하여 이용**
</aside>

### 확률 밀도 함수

---

![image.png](image%2082.png)

![image.png](image%2083.png)

### 분포

---

![y-0oGFVqkX8nzdRHnnXq8OmloMFi9G4xP7mgrS6EmNv9RX_tum5eyyGjHBHv-bwml6IFGZY54TEM5wPc4wqH-KZTi03H3PPJXbffJBLmv4DWUhMUumPDmHRtYZPI5yQZJIWuRSB_NWUeEztiRMuO7A.webp](y-0oGFVqkX8nzdRHnnXq8OmloMFi9G4xP7mgrS6EmNv9RX_tum5eyyGjHBHv-bwml6IFGZY54TEM5wPc4wqH-KZTi03H3PPJXbffJBLmv4DWUhMUumPDmHRtYZPI5yQZJIWuRSB_NWUeEztiRMuO7A.webp)

## 정리

---

![image.png](image%2084.png)

| z-검정 | σ^2을 알 때 μ를 구하는 것 |
| --- | --- |
| t-검정 | σ^2을 모를 때 μ를 구하는 것 |
| 카이-제곱 검정 | σ^2를 구하는 것 |
| f-검정 | σ1^2 / σ2^2 를 구할 때 |

## to be continued…

---

![제목 없음.png](%25EC%25A0%259C%25EB%25AA%25A9_%25EC%2597%2586%25EC%259D%258C.png)

![제목 없음2.png](%25EC%25A0%259C%25EB%25AA%25A9_%25EC%2597%2586%25EC%259D%258C2.png)