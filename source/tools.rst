工具
==================================================

ImageTrans还附带了一系列工具。

屏幕阅读器
++++++++++++++++

截取屏幕并OCR和翻译，所得的结果可以保存到项目中。支持检测剪贴板中的图片。OCR的结果会自动存入剪贴板。

.. image:: /images/screenreader.jpg

语音朗读器
++++++++++++++++

支持调用系统自带的TTS引擎朗读文本。


静默翻译器
+++++++++++++++++

可以以静默方式批量翻译图片，并支持终端调用。

终端调用方式：

``java -jar ImageTrans.jar configPath usePrevious detectOnly outdir fileListPath``

参数说明：

configPath：运行参数文件路径，内容为静默翻译器右侧显示的参数

usePrevious：是否使用之前的数据，可选值为true和false

detectOnly：是否仅检测文字区域，可选值为true和false

outdir：输出文件夹

fileListPath：待处理文件的列表，用换行分隔

可以搭配\ `ImageTrans_Server <https://github.com/xulihang/ImageTrans_Server>`_\ 提供在线服务


服务器
+++++++++++++++++

该工具可以允许其它软件调用ImageTrans翻译图片。

`ImageTrans Chrome插件 <https://github.com/xulihang/ImageTrans_chrome_extension>`_\ 需要使用这一功能。

该插件能用ImageTrans翻译网页中的图片，图片和处理结果会自动添加到ImageTrans当前的项目中。