快速入门
==================================================

软件安装
-----------

Windows完整版解压到任意目录后即可，Mac完整版打开dmg文件安装ImageTrans到应用目录即可。

需要使用Tesseract进行OCR的话请自行下载安装（`地址 <https://tesseract-ocr.github.io/tessdoc/Downloads.html>`_）。这里再提供一个Windows的绿色版本：`百度网盘（提取码：ktpt） <https://pan.baidu.com/s/1gJZyuntLetZEpFWI8XqkXA>`_。下载后将tesseract-ocr目录和ImageTrans放在一起。额外的语言包请放在 ``tesseract-ocr\tessdata`` 目录下。

本工具支持的在线OCR和机器翻译服务均需要设置API才能使用，其中谷歌翻译、云译和ocrspace为免费提供。付费用户还能获得百度和Azure的API。

以下内容是对于跨平台的版本：

下载ImageTrans的压缩包，解压到任意目录，双击ImageTrans.jar或者命令行输入 ``java -jar ImageTrans.jar`` 即可运行。

软件依赖JRE 1.8运行环境，请先下载安装。下载地址：1. `Liberica 8u275 full version  <https://github.com/bell-sw/Liberica/releases/tag/8u275%2B1>`_ 2. `百度网盘（提取码：mhsy） <https://pan.baidu.com/s/1t0g6htstFge0h2dOS0aBog>`_

软件依赖OpenCV，请根据系统下载运行库文件，解压后放在ImageTrans的目录下。下载地址：1. `GitHub <https://github.com/xulihang/ImageTrans-docs/releases/tag/opencv>`_, 2. `百度网盘 <https://pan.baidu.com/s/1D9EZMKqwgqQjdEjwYFkZQQ>`_


验证登录
------------

每次运行ImageTrans时，会显示验证器，需要填入购买时填写的email和订单号。订单号可以在收到的邮件中找到。

.. image:: /images/validator.jpg

一个email可以在三台设备上使用，要更换设备则需要使用邮箱进行重置。

.. image:: /images/reset_macs.jpg


新建项目
-----------

菜单栏点击文件-新建项目，选择一个位置并输入项目文件名以保存。

.. image:: /images/new_project.png


添加图片
++++++++++

菜单栏点击文件-导入图片文件夹，选择图片存在的位置。该操作会读取该文件夹下所有的子目录并导入存在的jpg、png文件。

.. image:: /images/import_images.png

或者用右键菜单-粘贴图片的方式添加单张图片。


文字转录
-----------

工具支持框选文字区域并识别。提供手动框选和四种自动框选，并支持精细调整文本框。

手动框选文字
+++++++++++++++++++

在图片上双击建立选择框，点住中间区域进行移动，点住右下角调整大小。

.. image:: /images/selectionbox.gif

或者点击左侧工具栏的快速框选按钮，可以直接滑动建框。

.. image:: /images/selectionbox_quickcreatin.gif

OCR
+++++++++++++++++++

选中文字区域，选择语言和OCR引擎，点击识别进行OCR。

.. image:: /images/OCR.gif

自动识别文字
++++++++++++++++++++++++++

选择语言和OCR引擎，点击菜单-编辑-自动识别文字，可以自动检测文字区域并转录。其中有道是按段落识别，其它引擎是按行识别，可以通过右侧编辑区域的合并左右区域和合并上下区域进行合并。

.. image:: /images/automatic_text_recognition.gif

自动识别气泡
++++++++++++++++++++++++++

选择语言和OCR引擎（仅限百度或者Azure），点击菜单-编辑-自动识别气泡，可以自动识别气泡。

.. image:: /images/balloon_detection.gif

另提供较为复杂的启发式和自然场景文字检测方法，详见 :ref:`text-detection`

自动OCR所有区域
++++++++++++++++++++++++++

我们可以先把文字区域框出，然后批量进行OCR。点击菜单-编辑-自动OCR所有区域进行操作。

排序
++++++++

支持根据坐标信息对文字区域进行排序。

.. image:: /images/sort.gif

导出
+++++++++++++

导出有多种选项。

.. image:: /images/export.png

* Tab分割的TXT文档，包含坐标信息、字体样式、文字等信息
* XLSX表格，和TXT的内容一样
* XLSX表格-根据目录建立工作表，按子目录保存图片名、原文和译文信息
* 所有文本，按每张图片生成包含图片文字的txt文档
* 供翻译的文档，将原文和译文信息以表格的形式导出为一个docx文档或者txt文档

翻译
-----------

在译文区域输入译文并点击保存可以完成一个文字区域的翻译。

可以将翻译导出为docx文档供外部人员翻译，之后再通过菜单-导回翻译-docx文档进行导回。

.. image:: /images/reimport.png

计算机辅助翻译软件BasicCAT支持直接操作ImageTrans的项目文件进行翻译。

翻译记忆、机器翻译和术语管理
+++++++++++++++++++++++++++++++++

切换右侧的操作区到辅助翻译页面，可以使用翻译记忆、机器翻译和术语管理这三个功能。机器翻译需要在偏好设置里设置API，并进行启用。另外还需要设置项目的语言，通过项目-设置-选择语言对进行设置。

.. image:: /images/CAT.jpg

预翻译
++++++++++++

点击菜单-项目-批处理-预翻译，可以使用翻译记忆或者机器翻译进行批量翻译。当前只支持机器翻译。

.. image:: /images/pretranslate.png


预览
+++++++++++

点击左下角的预览替换效果，可以预览翻译效果。选择精确模式会自动识别文字进行抹除并修复背景，非精确模式则会用背景颜色进行遮盖。

.. image:: /images/Preview.gif

勾选排版模式时，译文区域将被框出，并支持调整位置。

.. image:: /images/design_mode.jpg


生成成品图
--------------

首先将图片比例调整为100%，之后点击预览，得到成品图。点击文件-导出当前图片为-JPG，结果将输出在对应图片的文件夹的out文件夹中。另一选项ORA支持将文件导出为多层图像格式ORA，该格式能保存图层信息，供PS、Gimp和Krita等图像编辑软件编辑。

除此以外，ImageTrans可支持导出PSD。

设置文字样式
------------------

设置文字样式主要有两个作用，一个是在ImageTrans中进行预览，一个是用于导出PSD时设置字体。

点击菜单-项目-设置-字体样式可以进行设置使用的字体、文字大小、行距、对齐方式等等。

.. image:: /images/fontstyles.jpg

如果要修改某个样式，请点击该样式以加载设置，修改后点击添加，然后删去原来的样式。排在第一的样式是默认样式。

因为Photoshop需要的字体名比较特殊，需要从PS中获得。方法是在PS中新建一张图片，建立一个文本框，设置所需字体，并完成文字编辑操作，是文本框处于非编辑状态。之后在ImageTrans中点击读取即可。非Windows系统需要使用readFont.jsx脚本。

.. image:: /images/readPSfont.jpg

可以给文字区域设置专门的字体样式。

.. image:: /images/set_fontstyle.png

另外也支持设置本地样式，除了全局文字样式包含的内容外，支持描边和旋转角度的设置。设置本地字体样式时会调出全局字体样式的设置界面，默认读取添加在末尾的样式为本地字体样式。

.. image:: /images/localstyle.jpg

点击左侧的字体按钮以启用字体设置工具栏，可以便捷地设置本地样式。

.. image:: /images/fontstyle_bar.jpg

点击左侧的多选按钮以启动多选工具栏，可以调整多个文本框的位置并统一其字体样式。

.. image:: /images/selection_bar.jpg

批处理
--------------

以上对单个图片的操作都可以通过菜单-项目-批处理对所有图片进行操作。
