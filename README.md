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
> ### 1.Word Cloud 분석
<div>
 <img width="200" src="https://user-images.githubusercontent.com/74141344/102815924-87984180-4410-11eb-8e2a-57dabaa1e1d5.png">
 <img width="200" src="https://user-images.githubusercontent.com/74141344/102815982-9aab1180-4410-11eb-9bea-9baa1bdb94a0.png">
 <img width="200" src="https://user-images.githubusercontent.com/74141344/102815992-9da60200-4410-11eb-9d41-94af6b4f3d56.png">


Ⅳ.조사의 결론 및 시사점
-------------

