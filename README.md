# Convert-Any-File-To-Uint8Array
文件转 Uint8Array 转换工具

简介

本工具可以将任何文件格式转换为 Uint8Array，用于嵌入到 JavaScript 项目中。支持单文件转换和多文件/文件夹批量转换，输出结果以 .js 文件形式保存，方便直接在 JavaScript 中使用。
（Ps:建议还是不要一次性转换太多文件，文件太多会导致工具出现崩溃，虽然文件会继续转换但是无法确保完整性）
支持的文件格式
	1.	文本文件：
	•	.txt
	•	.csv
	•	.json
	•	.xml
	•	等其他文本格式
	2.	文档文件：
	•	.doc, .docx (Word)
	•	.pdf (PDF)
	•	.xls, .xlsx (Excel)
	•	.ppt, .pptx (PowerPoint)
	3.	图像文件：
	•	.jpg, .jpeg
	•	.png
	•	.bmp
	•	.gif
	•	.tiff, .tif
	4.	音频文件：
	•	.mp3
	•	.wav
	•	.flac
	•	.aac
	5.	视频文件：
	•	.mp4
	•	.avi
	•	.mkv
	•	.mov
	•	.wmv
	6.	压缩文件：
	•	.zip
	•	.rar
	•	.7z
	•	.tar
	•	.gz
	7.	任意二进制文件：
	•	可执行文件（.exe, .bin）
	•	动态链接库（.dll, .so）
	•	开发文件（.wasm, .jar）
	•	等其他非文本文件

工作原理

本工具通过 Python 的 open(input_path, "rb") 方法读取文件为字节流（bytes），将其逐字节转换为 Uint8Array 格式。文件的原始内容在转换中不会被解析或修改，确保通用性。

输出结果

对于每个输入文件，输出的 .js 文件内容形如：

const fileData = new Uint8Array([/* 文件的字节数组 */]);

这可以直接在 JavaScript 环境中用于加载或操作文件数据。

使用方式
	1.	运行程序。
	2.	在单文件模式下，拖拽或选择单个文件进行转换。
	3.	在多文件/文件夹模式下，选择多个文件或文件夹进行批量转换。
	4.	指定输出位置。
	5.	点击“开始转换”，生成的 .js 文件将保存到指定的输出位置。
