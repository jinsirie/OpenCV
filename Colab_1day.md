## test.ipynb
---


1. make image folder ( in Colabs)
```
!mkdir images
```


2. make model folder ( in Colabs)
```
!mkdir models
```



3. drag in pics for modeling
```
# age_net.caffemodel
!wget --no-check-certificate 'https://docs.google.com/uc?export=download&id=1PlZzJw-zq7ylzdl4PNxJyA1pvdGDBbOg' -O models/age_net.caffemodel

# deploy_age.prototxt
!wget --no-check-certificate 'https://docs.google.com/uc?export=download&id=12yOebfpUcO5eVLFOPj7oitPAq3ZNB6xl' -O models/deploy_age.prototxt
 
# gender_net.caffemodel
!wget --no-check-certificate 'https://docs.google.com/uc?export=download&id=1eqGU8hp8obD7fSB3Pu532jH9DNJd8uRY' -O models/gender_net.caffemodel
 
# deploy_gender.prototxt
!wget --no-check-certificate 'https://docs.google.com/uc?export=download&id=1qB4-vQchdYKzeezKkbT_j7LTlsAC2hqd' -O models/deploy_gender.prototxt
```


#Results
```
--2023-03-14 10:17:16--  https://docs.google.com/uc?export=download&id=1PlZzJw-zq7ylzdl4PNxJyA1pvdGDBbOg
Resolving docs.google.com (docs.google.com)... 172.253.62.113, 172.253.62.102, 172.253.62.100, ...
Connecting to docs.google.com (docs.google.com)|172.253.62.113|:443... connected.
HTTP request sent, awaiting response... 303 See Other
Location: https://doc-0o-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/vsjii8d1g5004h2bnm6tr6dl7rk653vp/1678788975000/02396526014819477879/*/1PlZzJw-zq7ylzdl4PNxJyA1pvdGDBbOg?e=download&uuid=355fd379-7713-4e26-a254-0c8a6980d76e [following]
Warning: wildcards not supported in HTTP.
--2023-03-14 10:17:17--  https://doc-0o-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/vsjii8d1g5004h2bnm6tr6dl7rk653vp/1678788975000/02396526014819477879/*/1PlZzJw-zq7ylzdl4PNxJyA1pvdGDBbOg?e=download&uuid=355fd379-7713-4e26-a254-0c8a6980d76e
Resolving doc-0o-1s-docs.googleusercontent.com (doc-0o-1s-docs.googleusercontent.com)... 142.250.31.132, 2607:f8b0:4004:c0b::84
Connecting to doc-0o-1s-docs.googleusercontent.com (doc-0o-1s-docs.googleusercontent.com)|142.250.31.132|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 45661480 (44M) [application/octet-stream]
Saving to: ‘models/age_net.caffemodel’

models/age_net.caff 100%[===================>]  43.55M  57.6MB/s    in 0.8s    

2023-03-14 10:17:18 (57.6 MB/s) - ‘models/age_net.caffemodel’ saved [45661480/45661480]

--2023-03-14 10:17:19--  https://docs.google.com/uc?export=download&id=12yOebfpUcO5eVLFOPj7oitPAq3ZNB6xl
Resolving docs.google.com (docs.google.com)... 172.253.62.113, 172.253.62.102, 172.253.62.100, ...
Connecting to docs.google.com (docs.google.com)|172.253.62.113|:443... connected.
HTTP request sent, awaiting response... 303 See Other
Location: https://doc-00-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/19sgsl2o8sekdmr4b2qhf6tnqhbvgg9i/1678788975000/02396526014819477879/*/12yOebfpUcO5eVLFOPj7oitPAq3ZNB6xl?e=download&uuid=4648e742-f0cf-453d-a0ed-bbf0ce83461e [following]
Warning: wildcards not supported in HTTP.
--2023-03-14 10:17:19--  https://doc-00-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/19sgsl2o8sekdmr4b2qhf6tnqhbvgg9i/1678788975000/02396526014819477879/*/12yOebfpUcO5eVLFOPj7oitPAq3ZNB6xl?e=download&uuid=4648e742-f0cf-453d-a0ed-bbf0ce83461e
Resolving doc-00-1s-docs.googleusercontent.com (doc-00-1s-docs.googleusercontent.com)... 142.250.31.132, 2607:f8b0:4004:c0b::84
Connecting to doc-00-1s-docs.googleusercontent.com (doc-00-1s-docs.googleusercontent.com)|142.250.31.132|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2308 (2.3K) [application/octet-stream]
Saving to: ‘models/deploy_age.prototxt’

models/deploy_age.p 100%[===================>]   2.25K  --.-KB/s    in 0s      

2023-03-14 10:17:19 (96.8 MB/s) - ‘models/deploy_age.prototxt’ saved [2308/2308]

--2023-03-14 10:17:19--  https://docs.google.com/uc?export=download&id=1eqGU8hp8obD7fSB3Pu532jH9DNJd8uRY
Resolving docs.google.com (docs.google.com)... 172.253.62.113, 172.253.62.102, 172.253.62.100, ...
Connecting to docs.google.com (docs.google.com)|172.253.62.113|:443... connected.
HTTP request sent, awaiting response... 303 See Other
Location: https://doc-0s-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/3dfltlpn2up6k6oim0lduvqnc94f0478/1678788975000/02396526014819477879/*/1eqGU8hp8obD7fSB3Pu532jH9DNJd8uRY?e=download&uuid=3a0e8eb4-9a6c-471e-b6bf-4204a37ff77a [following]
Warning: wildcards not supported in HTTP.
--2023-03-14 10:17:21--  https://doc-0s-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/3dfltlpn2up6k6oim0lduvqnc94f0478/1678788975000/02396526014819477879/*/1eqGU8hp8obD7fSB3Pu532jH9DNJd8uRY?e=download&uuid=3a0e8eb4-9a6c-471e-b6bf-4204a37ff77a
Resolving doc-0s-1s-docs.googleusercontent.com (doc-0s-1s-docs.googleusercontent.com)... 142.250.31.132, 2607:f8b0:4004:c0b::84
Connecting to doc-0s-1s-docs.googleusercontent.com (doc-0s-1s-docs.googleusercontent.com)|142.250.31.132|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 45649168 (44M) [application/octet-stream]
Saving to: ‘models/gender_net.caffemodel’

models/gender_net.c 100%[===================>]  43.53M  61.6MB/s    in 0.7s    

2023-03-14 10:17:22 (61.6 MB/s) - ‘models/gender_net.caffemodel’ saved [45649168/45649168]

--2023-03-14 10:17:22--  https://docs.google.com/uc?export=download&id=1qB4-vQchdYKzeezKkbT_j7LTlsAC2hqd
Resolving docs.google.com (docs.google.com)... 172.253.62.113, 172.253.62.102, 172.253.62.100, ...
Connecting to docs.google.com (docs.google.com)|172.253.62.113|:443... connected.
HTTP request sent, awaiting response... 303 See Other
Location: https://doc-0k-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/gu5hdptrid5ta3h5rg07ammg5cjtqpa3/1678788975000/02396526014819477879/*/1qB4-vQchdYKzeezKkbT_j7LTlsAC2hqd?e=download&uuid=cab133af-20c2-4f91-b94b-462a73db8529 [following]
Warning: wildcards not supported in HTTP.
--2023-03-14 10:17:22--  https://doc-0k-1s-docs.googleusercontent.com/docs/securesc/ha0ro937gcuc7l7deffksulhg5h7mbp1/gu5hdptrid5ta3h5rg07ammg5cjtqpa3/1678788975000/02396526014819477879/*/1qB4-vQchdYKzeezKkbT_j7LTlsAC2hqd?e=download&uuid=cab133af-20c2-4f91-b94b-462a73db8529
Resolving doc-0k-1s-docs.googleusercontent.com (doc-0k-1s-docs.googleusercontent.com)... 142.250.31.132, 2607:f8b0:4004:c0b::84
Connecting to doc-0k-1s-docs.googleusercontent.com (doc-0k-1s-docs.googleusercontent.com)|142.250.31.132|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2309 (2.3K) [application/octet-stream]
Saving to: ‘models/deploy_gender.prototxt’

models/deploy_gende 100%[===================>]   2.25K  --.-KB/s    in 0s      

2023-03-14 10:17:22 (87.8 MB/s) - ‘models/deploy_gender.prototxt’ saved [2309/2309]

```

5. Configure the downloads pics

```
!ls -al models
```

#Results
```
total 89188
drwxr-xr-x 2 root root     4096 Mar 14 10:16 .
drwxr-xr-x 1 root root     4096 Mar 14 10:05 ..
-rw-r--r-- 1 root root 45661480 Mar 14 10:17 age_net.caffemodel
-rw-r--r-- 1 root root     2308 Mar 14 10:17 deploy_age.prototxt
-rw-r--r-- 1 root root     2309 Mar 14 10:17 deploy_gender.prototxt
-rw-r--r-- 1 root root 45649168 Mar 14 10:17 gender_net.caffemodel
```


 6. do write python code for modeling ... 

 ```python
 import cv2,glob,dlib
from google.colab.patches import cv2_imshow

# 범위로 추정하기 때문에 아래와 같이 범위를 나누었다.
age_list = [ '(0,2)','(4,6)','(8,12)','(15,20)','(25,32)','(38,43)','(48,53)','(60,100)']

gender_list=['Male','Female']

#face 작업할때 가장 많이 사용하는 프레임워크
detector = dlib.get_frontal_face_detector()

#cv2.dnn 카페 모델을 손쉽게 불러오는 문구
age_net = cv2.dnn.readNetFromCaffe('models/deploy_age.prototxt','models/age_net.caffemodel')
gender_net=cv2.dnn.readNetFromCaffe('models/deploy_gender.prototxt','models/gender_net.caffemodel')

#glob 
img_list=glob.glob('images/*.jpg')

for img_path in img_list:

  img = cv2.imread(img_path)

  faces = detector(img)
#사진안에 여러 사람 얼굴이 있을 수 있다. 그래서 faces 안에 face 를 넣는다.
#정교할 수 없는 이유가 아래에 있다...
  for face in faces:
    x1,y1,x2,y2, = face.left(),face_top(),face.right(), face.bottom()
    face_img=img[y1:y2, x1:x2].copy

#네트워킹 할 준비
#scale factor=1 이라는 것은 정보량을 늘리지 않겠다는 것임 
#가로,세로 227 픽셀로 준비하는 것이다.
#얼마만큼 이 모델을 정밀도 높게 사용할 것인가 (평균치)
#레드와 블루와 반전을 할것인가 (swapRB)
  blob = cv2.dnn.blobFromImage(face_img,scalefactor=1, size(227,227),
                               mean(78.426337603, 87.7689143744, 114.895947746),
                              swapRB=False,crop=False)
  
  gender_net.setlnput(blob)
  gender_preds=gender_net.forward()  # 이미 사용하고 있는 사람들을 넣어준다.
  gender = gender_list[gender_preds[[0],argmax()]]


#softmax :argmax바꿔주는 활성함수, 후처리해준다.

 age_net.setlnput(blob)
 age_preds= age.net.forward()
 age = age_list[age_preds[0].argmax()]

 cv2.rectangle(img, (x1,y1),(x2,y2),(255,255,255),2)
 overlay_text='%s %s' %(gender,age)
 cv2.putText
 ```