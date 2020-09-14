## Face_detection and Face_scoring

### 文件组成

```markdown
两个人脸检测的库(不用管):
	1. dlib_face_recognition_resnet_model_v1.dat
	2. shape_predictor_68_face_landmarks

代码部分
	3. GetFace.py (利用上面两个库, 调用摄像头资源进行打分)
 	4. FaceppApi.py (调用face++的 API, 进行人脸打分)
 
文件保存
	5. faces文件夹保存获取的图像
```



### 使用说明

```markdown
注意事项
1. 路径使用的是相对路径, 应该不会有问题
2. GetFace.py import 了 FaceppApi。 因此直接运行GetFace.py即可
3. 注意, 每次运行程序默认都是从 person1 开始(这里不懂看代码), 因此，尽量只运行一次。若要运行多次，则必须	删除原来faces文件夹中的所有图片(放在别的地方也行，保证faces文件夹为空即可)


使用说明
4. 运行 GetFace.py 稍等一会儿就会调用摄像头资源. 首先按 N 键 创建文件夹(每个人单独一个文件夹，在faces	内部) , 摆好姿势后, 按 S 键存储当前图片, 稍等片刻即可输出识别结果(gender, age, male_socre, 	female_socre)
```



### 环境依赖

``` markdown
Anaconda3.7 + dlib + cv2 + numpy + urllib + json
```

