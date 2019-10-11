# leaflet study 1.html
这是一个非常简单例子，用来展示leaflet的基本使用方法。 
Basic usage of leaflet.

## 使用步骤
> 1. 引入leaflet的css和js
```
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.0.3/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet@1.0.3/dist/leaflet-src.js"></script>
```
> 2. body内定义一个用来表示地图的div要素。
```
<div id="map"></div>
```
> 3. 引入OpenStreetMap图层
> > 设置图层的中心点经纬度和地图放大倍数。[维度，经度]
```
var map = L.map('map').setView([34.255028, 108.942963], 14);
```
> 3. 引入OSM的图层到map对象
```
//引入OSM的图层到map对象。
var mapLink = '<a href="http://openstreetmap.org">OpenStreetMap</a>';
L.tileLayer(
	'http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
	{
		attribution: 'Map data &copy; ' + mapLink,
		maxZoom: 18
	}
).addTo(map);
```
