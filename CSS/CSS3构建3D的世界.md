CSS3示例网站
720yun.com
h5doo.com
========================================
H5 陀螺仪

z为轴 alpha [0,360]
x为轴 beta  [-180,180]
y为轴 gamma  [-90,90]
window.addEventListener("deviceorientation",function(event){

},true)
------------------------------------------
罗盘校准
window.addEventListener("compassneedscalibration",function(event){
	alert("you need jiaozhun");
	event.preventDefault();
},true)
--------------------------------------------------------------
重力加速度
window.addEventListener（"devicemotion",function(event){
    event.acceleration
    event.accelerationIncludingGravity
    event.rotationRate

},true）
-----------------------------------------
touch事件
css3d-engine
js库 Parallax

3d魔方