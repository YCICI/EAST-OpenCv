# EAST-OpenCv
 
 代码解释原地址：[https://www.pyimagesearch.com/2018/08/20/opencv-text-detection-east-text-detector/](https://www.pyimagesearch.com/2018/08/20/opencv-text-detection-east-text-detector/)
 
 下载代码可以通过原网站填写邮箱申请代码下载，但是有些时候会有延迟，而且之后会收到很多广告，所以就把我已经下好的代码放在这里
 提供给后来的朋友们下载。
 
 #### images detection
 
 检测的图片放在images/文件夹里，可以自行修改；  
 
 frozen_east_text_detection.pb是原论文作者训练好的模型，在文件夹中一并下载
````
 python text_detection.py --image images/lebron_james.jpg --east frozen_east_text_detection.pb
````

#### video detection
 ````
 python text_detection_video.py --east frozen_east_text_detection.pb
 ````
