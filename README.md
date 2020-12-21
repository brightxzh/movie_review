# Correlation_Analysis_between_FilmReview_and_Scandal
20-2 중국문화데이터포트폴리오 (HUFS)

201701981 중국언어문화전공 신희진

***

요약
-------------
* **주제** : 배우/제작진의 스캔들과 영화 평점별 리뷰의 상관관계
* **대상** : 영화〈불한당: 나쁜 놈들의 세상(2016)〉,〈지금은맞고그때는틀리다(2015)〉,〈밤의 해변에서 혼자(2016)〉,〈뮬란(2020)〉의 리뷰 21,570개
* **분석방식**
  1. 웹스크래핑으로 데이터 수집
  2. 형태소 분석기 KoNLPy 이용하여 데이터 정리
  3. Word Cloud와 Excel 피벗 테이블을 이용하여 분석
* **데이터 분석 및 해석 결과**
  1. 같은 키워드도 평점에 따라 다른 문맥에서 사용된다.
  2. 평점이 낮을수록 스캔들 관련 중심 키워드와 주변적 키워드가 모두 사용되고, 평점이 높을수록 '논란' 혹은 스캔들의 중심 키워드 몇 가지만 사용된다.
  3. 평점에 따라 서술어 어미 사용에 따라 어투의 공손함에서 차이가 있다.


***
***

프로젝트 설명
=============
Ⅰ.조사의 배경
-------------
  최근 영화계에서는 배우나 제작진에게 발생한 스캔들이 영화 리뷰의 평점 테러 운동으로 이어지는 현상이 나타나고 있다. 따라서 본 프로젝트는 작품과 연관이 없는 제작진의 스캔들이라는 요소가 영화 리뷰에 어떻게 나타나고 있는지를 살펴보고, 평점에 따라 리뷰 내용의 전개 양상을 파악해보고자 하는 목적을 가진다.
 
  조사의 신뢰성을 높이기 위하여 분석 대상인 영화 작품을 총 4가지로 선정하였다. 영화는 각각 **〈불한당: 나쁜 놈들의 세상(2016)〉**(이하 '불한당'으로 지칭) ,**〈지금은맞고그때는틀리다(2015)〉,〈밤의 해변에서 혼자(2016)〉**(두 작품을 묶어 이하 '홍상수 영화'로 지칭),**〈뮬란(2020)〉**(이하 '뮬란'으로 지칭)이다. 모두 개봉 전후로 한국 사회에서 제작진이나 배우의 스캔들이 발생하였던 작품이기 때문에 그와 관련한 내용이 영화 리뷰에서도 나타나고 있다. '불한당'은 감독인 변성현의 발언이 한국 사회에서 문제가 되었던 '일간베스트'(일베)와 연관되어 있으며 정치적인 성향을 노골적으로 드러낸다는 내용으로 논란이 되었다. '홍상수 영화'는 감독인 홍상수와 두 작품의 주연배우인 김민희의 불륜 스캔들로 논란이 되었다. '뮬란'은 주연배우인 유역비가 홍콩 경찰을 지지한다는 이유로, 저항정신을 나타내는 캐릭터인 뮬란 역에 적합하지 않다는 내용으로 논란이 되었다.
  

Ⅱ.데이터 수집 및 분석 방법
-------------
  조사에 이용한 데이터는 위에서 언급한 네 가지 작품에 대한 네이버 영화의 관람객 평점과 리뷰이며, 각 영화의 개봉일로부터 2020년 11월 1일까지의 리뷰가 포함되었다. 수집은 웹스크래핑 방식을 이용하였다. 수집한 리뷰는 한국어 형태소 분석기인 KoNLPy를 이용하여 형태소별로 정리하였으며, 이후 분석에서는 유의미한 키워드만을 볼 수 있도록 다음의 형태소만을 분석에 활용하였다. *Adjective, Adverb, Alpha, Exclamation, Foreign, Hashtag, Korean Particle, Modifier, Noun, Number, Verb* 분류 기준은 한국어에서 실질 형태소에 해당하는 품사이다. 정리된 자료는 각 영화당 1-3점, 4-7점, 8점-10점 3단계로 나누어 Word Cloud Generator에서 도출한 시각화 이미지와 Excel 피벗테이블을 이용해 그 내용을 분석하였다.
  
  
Ⅲ.데이터 분석 결과
-------------
>### 1.Word Cloud 분석
#### 가. 불한당: 나쁜 놈들의 세상(2016)
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102816492-713eb580-4411-11eb-8c95-4732edbf8ae3.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102816486-6f74f200-4411-11eb-8306-600658fec240.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102816489-70a61f00-4411-11eb-857f-980876fa5295.png">
  
평점 1-3점에서는 ‘일베’, ‘홍어’, ‘전라도’, ‘SNS', ‘트위터’, ‘인성’, ‘새끼’, ‘망한’, ‘쓰레기’, ‘재미없어요’, ‘재미없음’ 등의 키워드가 나타났다. 영화 자체를 폄하하는 키워드도 나타나지만, 감독의 언행 및 정치 성향 등 논란이 되었던 주제와 관련한 키워드가 다수를 이루었다. 

평점 4-7점에서는 ‘논란’, ‘그냥’, ‘킬링타임’, ‘그럭저럭’, ‘짬뽕’, ‘아쉽다’, ‘수준’, ‘솔직히’, ‘비슷한’, ‘괜찮은’, ‘그저’, ‘캐스팅’, ‘브로맨스’, ‘조폭’, ‘깡패’ 등의 키워드가 나타났다. 평점 1-3점이나 8-10점보다는 다소 영화 내적인 요소인 캐스팅이나 스토리와 관련한 키워드가 두드러지는 양상을 보였다.

평점 8-10점에서는 ‘느와르’, ‘연기’, ‘스토리’, ‘연기력’, ‘좋았습니다’, ‘였습니다’, ‘봤습니다’, ‘재밌었어요’, ‘좋았어요’, ‘보세요’ 등의 키워드가 나타났다. 평점 4-7점과 비슷하게 영화의 내부적 요소인 스토리나 배우의 연기력에 대해 언급하고 있지만, 주로 ‘좋다’, ‘재밌다’ 등의 긍정적인 감정 표현이 두드러진다.

‘감독’이란 키워드는 모든 평점에서 주요 키워드로 등장하는데 평점이 낮아질수록 더 크게 나타나고, 주연배우의 본명인 ‘임시완’, ‘설경구’의 키워드는 평점이 높아질수록 더 크게 나타나는 경향을 보였다. ‘신세계’, ‘프리즌’, ‘무간도’ 등 느와르 장르의 다른 영화제목 역시 모든 평점 구간에서 나타나고 있으나, 실제 원문을 분석하면 완전히 반대되는 문맥을 나타내고 있다. 높은 평점에서는 ‘불한당이 ㅇㅇ 영화보다 낫다’ 등의 의미로 언급되지만, 낮은 평점에서는 ‘감히 ㅇㅇ 영화와 비교를 하느냐’ 등의 의미로 언급되고 있다.
  
#### 나. 지금은맞고그때는틀리다(2015), 밤의 해변에서 혼자(2016) 
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
<img width="500" src="https://user-images.githubusercontent.com/74141344/102816781-ead6a380-4411-11eb-8ad4-65ffba7f6fcf.png">
<img width="500" src="https://user-images.githubusercontent.com/74141344/102816785-ec07d080-4411-11eb-9edf-59aad7aed330.png">
<img width="500" src="https://user-images.githubusercontent.com/74141344/102816788-eca06700-4411-11eb-8f14-1d8808cfc8fe.png">
  
 평점 1-3점에서는 ‘불륜’, ‘쓰레기’, ‘아깝다’, ‘미화’, ‘합리화’, ‘최악’, ‘더럽다’, ‘역겹다’, ‘싫다’, ‘간통죄’, ‘자식’, ‘부인’, ‘열자’ 등의 키워드가 나타났다. 홍상수 감독의 불륜 스캔들과 관련한 키워드가 주를 이루고 있다. 이중 ‘열자’의 키워드는 리뷰 작성 시 최소 기준인 열 글자를 쓰기도 귀찮다거나 시간이 아깝다는 의미에서 나타난 것이다. 평점 4-7점에서는 ‘그래도’, ‘좋았다’, ‘조금’, ‘지루한’, ‘변명’, ‘매력’, ‘틀리다’, ’사실’, ‘찌질’, ‘해변’ 등의 키워드가 나타났으며, 평점 8-10점에서는 ‘연기’, ‘정재영’, ‘배우’, ‘좋았다’, ‘대사’, ‘장면’, ‘일상’, ‘감정’, ‘봤습니다’, ‘좋았어요’, ‘합니다’ 등의 키워드가 나타났다.
 
전반적으로 ‘영화’, ‘감독’, ‘사랑’ 등의 키워드는 모든 평점 구간에서 많이 등장하고 있다. 스캔들과 관련된 인물인 ‘홍상수’와 ‘김민희’ 역시 모든 평점 구간에서 나타나지만 주로 높은 평점에서 더 크게 나타나고 있다. 낮은 평점에서 영화 외적인 요소인 스캔들에 대한 키워드가 많이 나타남에도 당사자의 이름이 적게 나타나는 것은 인물의 이름을 언급하기보다 ‘불륜’이나 ‘바람’ 등 다른 단어를 통해 언급하고 있기 때문으로 보인다. 이 때문에 ‘불륜’이라는 키워드는 낮은 평점에서 유독 크게 나타나고 있다. 4-7점과 8-10점에서 비교적 크게 나타나는 단어로는 ‘연기’와 ‘정재영’이 있는데, 배우 정재영의 경우 스캔들과는 관련 없이 해당 영화의 주연배우로서만 관련되어 있기 때문으로 보인다.

#### 다. 뮬란(2020)
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102815924-87984180-4410-11eb-8e2a-57dabaa1e1d5.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102815982-9aab1180-4410-11eb-9bea-9baa1bdb94a0.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102815992-9da60200-4410-11eb-9d41-94af6b4f3d56.png">
  
평점 1-3점에서는 ‘중국’, ‘홍콩’, ‘평점’, ‘free’, ‘hongkong’, ‘위구르’, ‘공산당’, ‘인권’, ‘자본’, ‘쓰레기’, ‘보이콧’, ‘최악’, ‘아깝다’, ‘2’, ‘3’ 등의 키워드가 주로 나타났다. 영화 개봉 당시 문제가 되었던 주연배우 유역비의 홍콩 경찰 지지 논란과 관련하여 홍콩 및 중국 내 소수민족과 중국 공산당에 관한 키워드가 주로 언급되었다. 여기서 2와 3이라는 키워드는 2D, 3D에서 나타난 것이며 원작인 2D 영화와 3D 영화인 해당 작품을 비교하고자 사용된 것으로 나타난다. 

평점 4-7점에서는 ‘아쉬움’ 솔직히’ ‘그저’, ‘논란’, ‘나름’, ‘자체’, ‘수준’, ‘중국무협, ‘실사영화’, ‘입니다’ 등의 키워드가 나타났다. ‘논란’이라는 키워드가 나타나긴 하지만 평점 1-3점과 달리 논란과 관련한 키워드들이 직접적으로 나타나지는 않는다. 대신 영화의 특성 및 작품성과 관련한 키워드가 주를 이룬다. 

평점 8-10점에서는 ‘액션’, ‘감동’, ‘감상’, ‘입니다’, 재미있게’, ‘좋은’, ‘좋았어요’, ‘봤습니다’, ‘였습니다’ 등의 키워드가 나타났다. 주로 ‘감동’, ‘좋다’ 등의 긍정적인 키워드가 나타나며 공손한 존대어 등의 어미 역시 주요 키워드에 포함되었다. 4-7점과 8-10점에서 ‘입니다’라는 키워드가 크게 나타나는 것을 통해 평점에 따라 리뷰 작성자들의 말투 역시 달라진다는 사실을 유추할 수 있었다.
 
#### 라. 전반적인 분석
평점이 낮을수록 스토리나 연기력, 작품성 등 내적인 요소보다는 제작진의 스캔들에 관련한 키워드가 다수 나타났다. 반면 평점이 높아질수록 배우의 연기력이나 감독의 연출 등 영화와 관련한 키워드가 주를 보이며, 긍정적인 키워드를 통해 리뷰 작성자의 감정이나 감상을 드러내는 양상도 나타났다.

평점 4-7점에서는 낮은 평점과 높은 평점에서 나타나는 키워드를 모두 볼 수 있다. 주로 영화 내적인 요소나 감정을 나타내는 키워드가 이러한 양상으로 나타났다. 반면 평점 4-7점에서 적게 나타나는 것은 영화와 관련된 스캔들에 관한 키워드이다. 평점이 낮은 경우에는 논란을 비판하고자 다수 언급하고, 평점이 높은 경우에는 ‘ㅇㅇ 논란은 아쉽지만’이라는 말을 덧붙이며 키워드가 언급되는 것을 확인할 수 있다. 높은 평점에서 가장 스캔들과 관련한 키워드가 적게 나타날 것이라는 기존 예측과는 달리, 평점 4-7점 구간에서 영화 내적 요소에 집중된 키워드가 가장 많이 나타남을 확인하였다.

또한 평점에 따라 리뷰를 작성하는 말투 역시 달라지는 것을 알 수 있었는데, 평점이 낮은 리뷰에 비해 평점이 높은 리뷰에서 ‘~니다’ 나 ‘~요’의 어미가 붙은 단어가 주로 나타난다. 이를 통해 비교적 공손하고 정제된 말투를 이용하여 영화 및 제작진에 대한 긍정적인 태도를 보여주고 있음을 알 수 있다. 일부 낮은 평점에서도 ‘~요’, ‘~니다’ 등의 어미가 붙은 키워드가 나타나기는 했지만, 이와 함께 사용되는 어휘를 보면 ‘보지+마세요’, ‘노잼+입니다’ 등 부정적인 감정을 담고 있는 것을 알 수 있었다. 또한 이러한 말은 영화나 제작진을 비판하고 리뷰를 보는 다른 네티즌들에게 의견을 전달하는 두 가지 목적이 있음을 보여준다.

>### 2. Excel 피벗 테이블 분석
#### 가. 불한당: 나쁜 놈들의 세상(2016)
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817130-85cf7d80-4412-11eb-94cf-5eb6c890335d.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817129-8536e700-4412-11eb-911d-f232c903bc3c.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817126-849e5080-4412-11eb-8df2-e5dc4033d848.png">
평점 1-3점에서는 스토리(1.576%), 생각(1.346%), 수준(0.987%), 별로(0.926%), 쓰레기(0.777%), 재미(0.654%), 돈(0.611%), 무간도(0.603%), 짬뽕(0.524%), 인성(0.521%), 여자(0.517%), 일베(0.460%) 등의 키워드가 타 구간에 비해 높은 빈도를 보였다. 이중 ‘여자’와 ‘일베’의 경우에는 영화와는 전혀 관련이 없는 감독의 발언과 관련한 키워드이다. ‘스토리’, ‘생각’, ‘재미’ 등 스캔들과 관련성이 적은 키워드는 4-7점 평점 구간과 비슷한 수치를 보인 반면, ‘수준’, ‘쓰레기’, ‘돈’, ‘인성’, ‘여자’ 등의 키워드는 다소 큰 차이를 보였다. 특히 ‘일베’의 경우엔 평점 4-7점에서의 수치가 매우 낮아 같은 표시 형식에서 수치를 확인할 수 없었다.
평점 4-7점에서는 연기(3.911%), 배우(9.161%), 설경구(2.901%), 신세계(2.283%), 그냥(1.503%), 느낌(1.373%), 내용(1.356%), 느와르(1.156%), 연기력(1.096%), 평점(1.032%), 연출(0.892%), 반전(0.646%), 결말(0.621%), 장면(0.611%), 작품(0.607%) 등의 키워드가 타 평점에 비해 높게 나타났다. Word Cloud에서 분석한 결과와 같이 주로 영화 내적인 요소인 연기, 스토리, 장르 등과 관련한 키워드가 다수를 이룬다. 다만 여기서 ‘그냥’이라는 키워드는 1-3점과 4-7점 평점에서 모두 높게 나타났는데 조합되는 어휘의 차이를 볼 수 있다. 1-3점에서는 ‘그냥’이라는 키워드가 ‘쓰레기’, ‘노잼’, ‘다른거 봐라’, ‘영화가 별로’ 등의 말과 붙어서 사용되는 반면, 4-7점에서는 ‘그냥+그래요’, ‘그냥+저냥’과 같이 사용되고 있었다.
평점 8-10점에서는 정말(0.766%), 최고(0.650%), 인생(0.327%), 홍어(0.309%) 등이 타 평점에 비해 높게 체크되었으며 느와르(1.055%), 평점(1.053%), 연출(0.851%) 등의 키워드는 4-7점과 비슷한 수치를 보였다. 여기서 ‘홍어’라는 키워드는 변성현 감독이 ‘홍어’를 비하 목적이 아닌 순수한 의도에서 사용하였다는 의미로 스캔들이 루머임을 주장하며 감독을 옹호하고자 사용되었다. 여기서 ‘자체’라는 단어는 8-10점에서 36번째로 자주 나타난 명사이지만, 수치는 1-3점에서 0.513%, 4-7점에서 0.835%, 8-10점에서 0.418%로 가장 낮게 나왔다. 주로 ‘영화 자체만 놓고 평가합시다’라는 의미에서 자주 사용되었다.

#### 나. 지금은맞고그때는틀리다(2015), 밤의 해변에서 혼자(2016) 
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817243-c3340b00-4412-11eb-9c4d-5d50f442fc7d.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817248-c4653800-4412-11eb-9572-bc5da5607299.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817246-c3cca180-4412-11eb-872a-a77ef0d513c0.png">
평점 1-3점에서는 불륜(1.737%), 예술(1.465%), 여자(0.802%), 평점(0.595%), 포장(0.607%) 등의 키워드가 타 구간보다 높은 빈도로 사용되었다. ‘불륜’의 경우, 해당 영화가 직면한 스캔들의 가장 중점적인 키워드라는 점에서 아주 높은 빈도로 사용되었음을 알 수 있었다. 또한, ‘예술’은 ‘이걸 예술이라고 하는 거냐’, ‘평점’은 ‘평점은 왜 이렇게 높냐,’ ‘포장’은 ‘포장 잘한다’ 등의 문맥에서 주로 사용된 단어였다. 
4-7점에서는 연기(2.475%), 생각(1.813%), 배우(1.321%), 이야기(1.133%), 현실(0.758%) 등의 키워드의 빈도가 높게 나타났다. 〈뮬란(2020)〉과 마찬가지로 Word Cloud에서 살펴본 것과 같이, 해당 평점 구간에서는 주로 연기나 배우, 스토리 등 영화 내적인 요소에 관한 키워드나 자신의 의견을 말하는 단어가 주를 이루고 있었다. 
8-10점에서는 정재영(1.005%), 작품(0.728%), 역시(0.635%), 매력(0.547%), 최고(0.472%) 등의 키워드가 자주 등장했다. 이에 대해서는 긍정적인 어감을 가진 단어가 많이 쓰임을 알 수 있었다. ‘정재영’의 경우엔 주연 배우의 연기력을 칭찬하기 위해 사용한 경우가 대다수였다.

#### 다. 뮬란(2020)
왼쪽부터 평점 1-3점, 4-7점, 8-10점이다.
<div>
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817299-dfd04300-4412-11eb-9cb3-6146283cf42f.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817297-dfd04300-4412-11eb-82a0-e602f5020df9.png">
 <img width="500" src="https://user-images.githubusercontent.com/74141344/102817294-df37ac80-4412-11eb-8579-775239322c89.png">
평점 1-3점에서는 타 평점 구간과는 달리 중국(2.635%), 영혼(2.507%), 그냥(1.339%), 디워(1.159%), 무협(0.955%), 돈(0.572%), 별로(0.610%), 실망(0.544%) 등의 키워드의 빈도가 더 높게 나타났다. 이 중에 ‘디워’라는 키워드는 해당 구간에서만 나타났는데, 영화 ‘디워’ 수준으로 망한 영화라는 의미로써 사용된 것이다. ‘영혼’이란 키워드는 자본 및 중국에 영혼을 판 영화란 의미에서 사용되었다.
평점 4-7점에서는 원작(2.991%), 감상(2.138%), 액션(1.743%), 스토리(1.611%), 애니(1.597%), 생각(1.524%), 실사(1.256%), 느낌’(1.165%), 상미(0.923%), 노래(0.920%), 장면(0.869%), 캐릭터(0.859%), 배우(0.859%) 등의 키워드의 빈도가 타 평점보다 높게 나타났다. 앞서 Word Cloud에서 보았던 영화 내적 요소와 관련된 주요 키워드가 모두 평점 4-7점에서 가장 많이 나타남을 알 수 있다. 특이점은 원작이나 애니, 실사 등의 키워드가 자주 나타나면서 원작인 애니메이션과 실사영화인 이 작품을 비교하는 리뷰가 많다는 것이다. 여기서 ‘상미’라는 키워드는 영상미를 의미하는 것이며, 영상미가 괜찮다 혹은 별로다 등 관련한 내용은 다양하게 분포하고 있다.
평점 8-10점에서는 은근(1.224%), 감동(1.214%), 평점(0.732) 등의 키워드가 높게 나타났다. 특이점은 ‘논란’이란 키워드가 유일하게 높은 평점에서 주요 키워드 50위 안에 포함되었지만 언급된 빈도는 가장 적다. (1-3점: 0.426, 4-7점: 0.465 / 8-10점: 0.369)


Ⅳ.조사의 결론 및 시사점
-------------

