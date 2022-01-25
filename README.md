# Every Document Owns Its Structure: Inductive Text Classification via Graph Neural Networks (textING)
* 논문 링크: <https://arxiv.org/pdf/2004.13826v2.pdf>


## Data
* Click [here] (https://github.com/e9t/nsmc)
* 200K reviews in total
- ```ratings_test.txt```: 50K review held out for testing
- ```ratings_train.txt```:150K reivews for training
* For each file
- ```id```:The review id, provided by Naver
- ```document```:Actual review
- ```label```: The sentiment class of the review (0: negative, 1: positive)

## Model
* 논문 내 모델 구현
* ```Tensorflow``` 사용

## Preprocessing
* ```Mecab``` 사용
```!set -x \
&& pip install konlpy \
&& curl -s https://raw.githubusercontent.com/konlpy/konlpy/master/scripts/mecab.sh | bash -x 
```

## Result
```Classify('진짜 재미없다.')
[진짜 재미없다.] is a NEGATIVE review !!
Classify('영화가 너무 재미있었어요!')
[영화가 너무 재미있었어요!] is a POSITIVE review !!
Classify('재미있는 것 같기도 하고, 재미 없는 것 같기도 하고, 적당했어요.')
[재미있는 것 같기도 하고, 재미 없는 것 같기도 하고, 적당했어요.] is a POSITIVE review !!


