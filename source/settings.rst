软件设置
==================================================



通用设置
-----------

.. _balloon-detection:

气泡检测
+++++++++++++


本工具的气泡检测支持调用基于Darknet Yolo或者TensorFlow Object Detection API训练的离线气泡检测模型，需要将模型放在软件的目录中并在菜单-文件-偏好设置-通用里启用离线气泡检测。

现有的离线模型：\ `日漫气泡识别模型 <https://github.com/xulihang/ImageTrans-docs/issues/135>`_。

此外也能使用百度EasyDL和微软Azure的目标检测服务。需要自行开通账号并训练。

推荐的标注方法：

选中所有气泡中的文字，选框尽量贴合文字。

.. image:: /images/image_annotation.JPG

发布模型后，在菜单-文件-偏好设置-API里设置发布了的URL，同时还需要填写对应的API。


文字图像识别
++++++++++++++

软件默认调用本地模型识别文字和非文字区域。此外也可以调用API服务。

默认地址为：`<http://127.0.0.1:8082/classify>`_

请运行以下仓库的代码： `<https://github.com/xulihang/text-image-classifier>`_。

自然场景文字检测
+++++++++++++++++++++++

支持使用EAST和CRAFT自然场景文字检测方法进行文字检测。

默认地址为：`<http://127.0.0.1:8080/detect>`_

代码地址： `<https://github.com/xulihang/ImageTrans_SceneText_Detection>`_。


API设置
-----------

点击菜单-文件-偏好设置-API，可以设置百度、有道、微软、腾讯等OCR和机器翻译服务提供商的API。

.. image:: /images/api_setting.jpg

下面是需要设置API密钥的服务的列表。

OCR:

* `Google <https://cloud.google.com/vision/docs/ocr>`_
* `Clova <https://clova.ai/>`_
* `百度 <https://cloud.baidu.com/product/ocr_general>`_
* `腾讯 <https://cloud.tencent.com/product/generalocr>`_
* `有道 <http://ai.youdao.com/product-ocr-print.s>`_
* `OCRSPACE <https://ocr.space/OCRAPI>`_
* `微软Azure <https://azure.microsoft.com/zh-cn/services/cognitive-services/computer-vision/>`_


机器翻译见BasicCAT的\ `文档 <https://docs.basiccat.org/en/latest/advancedFeatures.html#id2>`_。

外观设置
-----------

点击菜单-文件-偏好设置-主题可以对外观进行设置，除了默认主题，还有黑色、绿色主题。

此外也能利用CSS调整软件的外观。

例如以下CSS文件能够控制文字编辑区域的文字大小：

::

    .text-area {
        -fx-font-size: 25 !important;
    }


文本编辑区域的字体也能在项目设置中修改。
