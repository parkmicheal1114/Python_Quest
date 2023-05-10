# Code Peer Review Templete
- 코더 : 박기용, 노유현
- 리뷰어 : 신노아


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.
- [x] 1.코드가 정상적으로 동작하나요?
- [X] 2.문제를 제대로 이해했나요?
- [X] 3.함수가 작동하는 방식을 잘 설명했나요?
- [X] 4.발생 가능한 에러를 찾아서 디버깅을 했나요?
- [X] 5.코드를 더 개선시켰나요?

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 소문자 lower()
# from collections import Counter
# 파일 불러오기 
with open('/content/drive/MyDrive/Colab Notebooks/06TheAvengers.txt','r') as f:
  data = f.read()

print(len(data))
     

# Counter 임포트 하기
from collections import Counter
     

# 소문자 변화하기 
data_lower = data.lower()
data_lower
     


# remove_char = [",","-",".","\n","...","?","!"]


# for char in remove_char:
#   data_reform = data_lower.replace(char," ")
     
```

# 참고 링크 및 코드 개선 여부
```python
# colab 작동이상으로 마무리가 안되어 아쉬워하셨는데 colab만 작동 잘 되었으면 완벽하게 잘 되었을 듯 합니다.  
# 
#
#
```

