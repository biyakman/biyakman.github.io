---
title: "Imitation learning for language generation from unaligned data"
date: "2019-12-07"
categories: NLG Imitation_learning
---

##### 2019 NIPS tutorial  [눈문바로가기](https://www.aclweb.org/anthology/C16-1105.pdf)

* 목적 

    자연언어 생성 시 예측공간 줄이기

* 기존 연구의 문제점

    LSTM은 cross entropy를 사용하며, 현재 예측 대상인 단어와 후에 예측할 단어들 간의 interactions 학습 불가능

* 제안 기법

    Imitation Learning Locally Optimal Learning to Search(LOLS) 기법으로 Unaligned data학습 -> 
    sentence planning & surface realization

* 제안 기법의 장점

    * LOLS는 greedy 방식으로 추론을 하기 때문에 structured prediction이 감소
    * non-decomposable Loss 함수 사용 가능 -> BLEAU, Rougue에 적합
    * 현재 예측 대상인 단어와 후에 예측할 단어들 간의 interactions 학습 가능

    



###### 모르는 키워드
* ###### meaning representation, aligned training data, phrase template, surfaec realization, structured prediction