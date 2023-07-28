# AIFFEL Campus Online 4th Code Peer Review Templete
- 코더 : 박기용
- 리뷰어 : 노유현

# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.
- [O] 1.코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [O] 2.주석을 보고 작성자의 코드가 이해되었나요?
  > 물론입니다. 코더님꼐서 주석을 자세하지만 간결하게 작성해 주셔서 이해하기에 용이하였습니다. 
- [X] 3.코드가 에러를 유발할 가능성이 있나요?
  > 코드의 애러는 없었습니다. 
- [O] 4.코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 코더님은 이해 뿐만 아니라, 기존에 배운 내용의 코드에 더해 코드를 응용하셔서 한꺼번에 데이터 결과를 출력할 수 있도록 코드를 작성하였습니다.
- [O] 5.코드가 간결한가요?
  > 코드가 군더더기 없이 간결하여, 추가 설명이 없어도 코드만으로도 이해가 잘 되었습니다. 

# 코드

```python
def shallow_focus(img_dir , blur = 13 , reverse = False):

    for img_file in img_dir:   

        # Read file
        img = os.path.join('/aiffel/image/',img_file)
        img_orig = cv2.imread(img)  

        # Pascalvoc 
        segvalues, output = model.segmentAsPascalvoc(img)
        
        # class id
        id = [class_id for class_id in segvalues['class_ids']]
        
        # class id 별 이미지 출력
        for i in range(len(id)):
            
            # RGB => BGR color map 변환
            r,g,b = colormap[id[i]]
            seg_color = (b,g,r) 

            seg_map = np.all(output==seg_color, axis=-1) 


```

# 참고 링크 및 코드 개선
```python
# 다양한 이미지 데이터를 불러와서 출력 결과를 비교, 분석할 수 있었고 결과에 대한 다양한 고찰을 하셔서 모델에 대한 이해도를 높였습니다.
# 다양한 이미지 데이터를 한꺼번에 돌릴 수 있는 코드를 구현하였으며, 코드가 간결하고, 여러가지 코드를 다양하게 구현하셨습니다.
# 참조 사이트
