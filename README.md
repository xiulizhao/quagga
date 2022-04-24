# quagga
 条形码扫描器元素, 用于实现点击扫描条形码的需求<br>
 <img src="http://www.wware.org/img/txmsmq.png?_2e0e" width="400px"><br>
普通属性<br>
data-width	设置视频流(屏幕)宽度,宽度选项是单个条的宽度。例如375 单位像素	375<br>
data-height	设置视频流(屏幕)高度.例如640 单位像素。	50<br>
data-facingmode	设置前置和后置摄像头.例如前置user ,后置environment。默认为后置摄像头	user/environment<br>
控制属性<br>	
data--echartsoption	后端返回项目数据源:json数组	{"tooltip":{"formatter":"{a} <br></div>{b} : {c}%"},"series":[{"name":"业务指标","type":"gauge","endAngle":-45,"detail":{"formatter":"{value}%"},"data":[{"value":55,"name":"完成率"}],"axisLine":{"lineStyle":{"width":30,"color":[[0.3,"#f9402c"],[0.7,"#edae01"],[1,"#048807"]]}}}]}<br>
输出属性<br>
data-x-quaggavalue	输出扫描条形码的内容。	123456780912<br>
# 注意事项
1、点击启动扫描可以自己自定义按钮文字等.注意是在 class="canvanCode"div内设置填写。<br>
2、点击启动之后会出现像是照相功能的界面,对准条形码即可扫描成功.采用的是视频流效果。<br>
3、可用通过输出属性获取条形码内容。<br>
4、设置视频流在手机端视频的样式,如宽,高等<br>
```css
video {
 min-width: 100%!important;
 min-height: 100%!important;
 object-fit: cover!important;
 }
 .canvanCode {
 margin:0 auto;
 width: 220px!important;
 height: 220px!important;
 overflow: hidden!important;
 }
 .canvanCode canvas, video {
 width: 220px;
 height: 220px;
 }
 
```
