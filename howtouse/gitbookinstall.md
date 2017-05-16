Gitbook安装
====
leaflet加载google地图
效果
![](/imgs/googlemap_leaflet.jpg)
具体代码实现
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<link href="https://cdn.bootcss.com/leaflet/1.0.3/leaflet.css" rel="stylesheet">
		<script src="https://cdn.bootcss.com/leaflet/1.0.3/leaflet.js"></script>
		<style type="text/css">
			*,
			html {
				padding: 0;
				margin: 0;
			}
			
			#mymap {
				position: absolute;
				width: 100%;
				height: 100%;
			}
		</style>
	</head>

	<body>
		<div id="mymap"></div>
		<script type="text/javascript">
			let map = L.map('mymap').setView([30.285159872426014, 120.1633071899414], 12);

			L.tileLayer('http://www.google.cn/maps/vt?lyrs=m@189&gl=cn&x={x}&y={y}&z={z}').addTo(map);
		</script>
	</body>

</html>
```
##### 三、参考文献与网站

参考网站[](http://www.knowsky.com/610033.html)
