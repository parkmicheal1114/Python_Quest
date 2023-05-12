# Code Peer Review Templete
- 코더 : 박기용, 노유현 
- 리뷰어 : 신노아


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [v] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [v] 주석을 보고 작성자의 코드가 이해되었나요?
- [ ] 코드가 에러를 유발할 가능성이 있나요?
- [v] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [v] 코드가 간결한가요?

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

