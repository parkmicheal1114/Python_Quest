# AIFFEL Campus Online 4th Code Peer Review Templete
- 코더 : 박기용
- 리뷰어 : 노유현

# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.
- [O] 1.코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [O] 2.주석을 보고 작성자의 코드가 이해되었나요?
  > 물론입니다. 코더님꼐서 주석을 자세하지만 간결하게 작성해 주셔서 이해하기에 용이하였습니다. 
- [X] 3.코드가 에러를 유발할 가능성이 있나요?
  > 코드의 애러는 없었습니다. 코드가 잘 동작했고 높은 성능을 도출하였습니다. 
- [O] 4.코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 코더님은 이해 뿐만 아니라, 코드를 다양하게 응용하여 더 높은 성능을 도출하였습니다.  
- [O] 5.코드가 간결한가요?
  > 코드가 군더더기 없이 간결하여, 추가 설명이 없어도 코드만으로도 이해가 잘 되었습니다. 

# 코드

```python
# VGG16 ( Fine Tuning)

# Freezing 할 레이어 화인
for idx , block in enumerate(vgg16.layers):
  print (idx , block)


# VGG16 모델 불러오기
vgg16 = VGG16(input_shape=(IMG_SIZE,IMG_SIZE,3), include_top=False, weights="imagenet")

# freeze_index 설정하기
freeze_index = 15 # block5_conv1 레이어의 인덱스

# freeze_index 이전의 층은 고정하고, 이후의 층은 학습 가능하게 설정하기
for layer in vgg16.layers[:freeze_index]:
    layer.trainable = False
for layer in vgg16.layers[freeze_index:]:
    layer.trainable = True


# FC Layer 추가하기
model = Sequential()
model.add(vgg16)
model.add(GlobalAveragePooling2D())
model.add(Dense(512, activation='relu'))
model.add(Dense(2, activation='softmax'))
model.compile(loss = tf.keras.losses.sparse_categorical_crossentropy,
              optimizer = tf.keras.optimizers.RMSprop(learning_rate=1e-4), metrics=['accuracy'])

```

# 참고 링크 및 코드 개선
```python
# VGG16 모델을 활용하여 93%의 정확도를 보였고, 다시 Fine Tunning을 통해 97%까지 정확도를 달성하였다. 
# 코드가 완벽하여 코드 리뷰를 통해 수정할 부분은 없었고, 성능을 개선시키기 위해 다양한 시도를 하였고, 97%의 모델 성능은 감탄스러웠다. 
# 참조 사이트
https://www.tensorflow.org/datasets/catalog/cats_vs_dogs?hl=ko
https://www.tensorflow.org/datasets/overview?hl=ko

```
