# dyndelogo
ffmpeg dyndelogo module for remove watermark dynamically.

ffmpeg水印动态检测与删除模块程序

# description
I have written a dyndelogo module for ffmpeg, it could detect the position of watermark and remove it dynamically. it can be used to remove the code from IPTV stream. or similiar video file. the speed is quite high, in a E5 8 cores server, and process with 720P video stream, it can process 30~35 fps. but, it has disadvantage, it can be used to detect the watermark with fixed size only. because to make the speed as fast as possible. even in real-time. opencv or other OCR library is very slow. my first version program is using tesseract-ocr, I get only 3 fps, my second version is used libccv, it's more faster. about 8 fps.  but still slowly.

我在前几个月为我的一个IPTV客户写了一个动态水印删除程序, 最后根据我的经验, 我在ffmpeg的基础上修改了源代码, 添加了一个dyndelogo模块,以实现水印的动态检测与删除. 而且这个程序能够实时地处理任何输入流或者视频文件, 在一个8核的Xeon E5服务器上，处理720P视频可以达到35 fps. 这是opencv与其他库不能达到的. 当然我的程序本身并没有像opencv那样使用矩阵变换等高级的算法, 因为大部分水印的大小是固定的,他并不像人脸识别那么复杂.任何C程序员都可以写出来或许我写的更好.

If you want to get this software, you can contact me via email: yzfedora@gmail.com, test sample video will be provided on bellow.

test video before processing: https://youtu.be/KacC1omWcN0

test video after  processing: https://youtu.be/Dj2wCTAYDLU

(it's a crazy test, the test video will generate a watermark text "Hello, World" in a random position 25 times per second, normally in a product environment, you never seen some video like this, at least it's really crazy).
