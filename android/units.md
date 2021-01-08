android view units
==================

레이아웃: wrap_content, match_parent, dp 사용 권장   
텍스트: sp, dp 사용 권장

### [화면]
### 화면 크기
- 화면의 실제 물리적 크기
- 화면의 대각선 크기로 측정
- 일반화된 네 가지 크기 그룹으로 분류

  > 초대형 화면: 최소 960 dp x 720 dp   
  > 대형 화면: 최소 640 dp x 480 dp   
  > 보통 화면: 최소 470 dp x 320 dp   
  > 소형 화면: 최소 426 dp x 320 dp

### 화면 밀도(dots per inch, dpi)
- 물리적 화면 공간 안에 있는 픽셀의 개수
- 일반화된 여섯 가지 밀도 그룹으로 분류
  
  > ldpi (저밀도): ~ 120 dpi   
  > mdpi (중간 밀도): ~ 160 dpi   
  > hdpi (고밀도): ~ 240 dpi   
  > xhdpi (초고밀도): ~ 320 dpi   
  > xxhdpi (초초고밀도): ~ 480 dpi   
  > xxxhdpi (초초초고밀도): ~ 640 dpi

### 해상도(화소)
- 화면에 있는 물리적 픽셀의 총 개수

### [단위]
### 1. px
- 화면 픽셀
- 픽셀 단위로 크기 지정 시 화면 밀도가 큰 화면에서는 요소들이 작게 보여짐

### 2. dp/dip (가장 많이 사용)
- 160dip 화면을 기준으로 한 픽셀, 보통 밀도 화면에 해당하는 기준 밀도
- px = dp x (dpi / 160)
  
  > 예) 1인치 당 160개의 점이 있는 디스플레이: 1dp = 1px   
  > 1인치 당 320개의 점이 있는 디스플레이: 1dp = 2px
  
### 3. sp/sip (가장 많이 사용)
- 가변 글꼴을 기준으로 한 픽셀
- dp와 유사하나 글꼴의 설정에 따라 달라짐

### 4. in
- 1인치로 된 물리적 길이
  
### 5. mm
- 1밀리미터로 된 물리적 길이
    
### 6. em
- 글꼴과 상관없이 동일한 텍스트 크기 표시 표시
---
&reference
- [android view units](https://offbyone.tistory.com/229)