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
# Fish 객체 생성.
# 클래스로 객체 생성
class Fish:
  def __init__(self,name,speed ):
    self.name = name
    self.speed = speed

# comprehension.
# 컴프리헨션 사용
def show_fish_movement_comprehension(fish_list):    
  [print(f"{fish.name} is swimming {fish.speed} m/s") for fish in fish_list] 

# iterator.
# 이터레이터 사용
def show_fish_movement_iterator(fish_list):   
  for fish in fish_list:
    print(f"{fish.name} is swimming {fish.speed} m/s")

# generator,
# 제너레이터 사용
def show_fish_movement_generator(fish_list):   
  for fish in fish_list:
    print(f"{fish.name} is swimming {fish.speed} m/s")
    yield
     

# fish_list 
# 물고기 리스트 생성
fish_list = [
    Fish("Nemo", 3),
    Fish("Dory", 5),
    Fish("Marlin", 7),
    Fish("Bubbles", 2),
    Fish("Gill", 4)
]

# 컴프리핸션 결과값
# 결과값 출력
print("Using Comprehension:")
show_fish_movement_comprehension(fish_list)

# 이터레이터 결과값
print("\nUsing Iterator:")
show_fish_movement_iterator(fish_list)

# 이터레이터 결과값
print("\nUsing Generator:")
generator = show_fish_movement_generator(fish_list)
for _ in generator:
  pass

     
Using Comprehension:
Nemo is swimming 3 m/s
Dory is swimming 5 m/s
Marlin is swimming 7 m/s
Bubbles is swimming 2 m/s
Gill is swimming 4 m/s

Using Iterator:
Nemo is swimming 3 m/s
Dory is swimming 5 m/s
Marlin is swimming 7 m/s
Bubbles is swimming 2 m/s
Gill is swimming 4 m/s

Using Generator:
Nemo is swimming 3 m/s
Dory is swimming 5 m/s
Marlin is swimming 7 m/s
Bubbles is swimming 2 m/s
Gill is swimming 4 m/s 
```

# 참고 링크 및 코드 개선 여부
```python
#문제에 대한 이해를 완벽히 하셨고 작성하신 코드도 매우 잘 작동됩니다.
#
#
#
```

