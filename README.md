# 01-JS-Drum-Kit:drum:
> JS 30 Challenge는 제공되는 index-START.html, syle.css를 기본으로 JS 코드를 구현하는 challenge 입니다.  

:triangular_flag_on_post: JS 30 days Challenge - 1/30 Drum kit  

### 기능
- 기본 기능
  - 키보드 입력 시, 해당하는 sound 출력 :heavy_check_mark:

### index-START.html의 \<body> 구성

```html
  <div class="keys">
    <div data-key=(keyCode_값) class="key">
      <kdb>(keyCode_값)</kdb>
      <span>(sound_이름)</span>
    </div>
    ... // 총 9개
  </div>
  
  <audio data-key=(KeyCode_값) src=(해당_sound의_경로) />
  ... // 총 9개
``` 

### 설계
|기능|설계|
|---|---|
|키보드 입력 시, 해당하는 sound 출력|1) 키보드 입력 시의 리스너 객체 구현 <br>  - 입력한 keyCode와 같은 data-key를 가지는 \<audio>를 가져옴 <br>  - 가져온 audio 출력|
|키보드 입력 시, 해당하는 sound \<div>에 css border 속성 추가|1) 키보드 입력 시, 제공 css 파일에 따라 \<div>의 classList에 'playing' 추가 <br>2) css 변경 후에 적용되는 이벤트의 리스너 객체 구현 <br>  - 변경된 요소의 classList에 'playing' 존재 여부 확인 <br>  - 존재 시, 'playing' 삭제|

### 실행 방법
1) 해당 repository의 index.html 파일 실행  
2) A, S, D, F, G, H, J, K, L 키를 사용해 드럼 비트 찍기  

![JS Drum Kit](https://user-images.githubusercontent.com/48666975/102196036-b25f3300-3f02-11eb-9d1c-23dbe111d370.PNG)
