人脸识别接口说明

人脸识别API：  QQ493572374

1: 人脸比对接口

参数：image1  图片1 base64 
	  image2  图片2 base64

请求格式 post json {"image1":"base64","image2":"base64"}  

url:  http://120.79.141.218:9998/facecompare

返回格式：
		threshold 参考阈值
		validate_result 判断是同一个人 1 表示同一个 0 表示不是同一个人或者比对失败
		reason 比对成功
		error_code  返回码
		similarity  相似度
		
返回结果：{"threshold": "0.53", "validate_result": "1", "reason": "success", "error_code": "0", "similarity": 100}

1：人脸提取特征接口
参数 ：image 图片 base64

请求格式post json {"image":"base64"}

url:  http://120.79.141.218:9998/getfeature

返回格式：
		image 特征值

		

例子：请求示例
见  人脸比对 post_cmp.py
	提取特征 post_getfeature.py

直接运行 python post_cmp.py 即可

