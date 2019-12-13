---
title: "code 의문 list"
date: "2019-12-13"
categories: code
---
[code](https://github.com/Intelligence-Engineering-LAB-KU/TIF-Enhanced-Self-Attentive-Net/blob/master/MSS-Baseline.ipynb)
## tensor shape (ln 4)
* (batch 크기, channel 수, frequency, stft frame)
    *  (4, 4, 2048, 128)
* [ ] frequency bin 이해
* [ ] stft frames

## STFT parameters and functions (ln 5)
* [ ]  실수부 허수부 나누는거
* [ ]  n_fft 파라미터

* to_specs 함수 (스펙트로그램 변환 함수)
  * signal 받아서 librosa 라이브러리의 stft 변환 함수 사용
      * stft변환하여 실수부 허수부에 append
      * 변환전 : ((channel, 데이터타입), n_fft, center, hop_length)
        * ((?, float), 4096, false, 1024)
        * [ ] 이게스펙트로그램 shape 은 아닐것 같은데?
      * specs(spectogram) 배열 반환
      * 


* restore 함수
  * 스펙트로그램 reshape specs 받아서 (-1, 2, dim_f+1, dim_t)로 변환
    * (-1, 2, 2049, 2048)
    * [ ] dim_f+1 하는 이유
  * channels 초기화
  * 스펙트로그램의 각 ri_real, ri_imag 에 대하여
    * [ ] ri 뭣의 약어?
    * signal에 librosa.istft 함수로 복원 (Inverse short-time Fourier transform)
    * np.array(channels) 채널 배열로 묶어서 반환

* chunk 함수
  * np.random.randint
  * Return random integers from low (inclusive) to high (exclusive).
  * [ ] frame 의 카디널리티 



)
    
    





  


