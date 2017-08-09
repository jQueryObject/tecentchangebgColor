# 腾讯空间背景换肤tecentchangebgColor
效果如下：
![](images/img.gif)

all code:
```
<!--文档声明为 html（最新html5）-->
<!doctype  html>
<html>
	<head>
		<!--声明当前页面编码格式为国际编码（utf-8）还有一种中文编码（gbk/gb2312）-->
		<meta charset="UTF-8">
		<!--网页三要素-->
		<meta name="Keywords" content="关键词,关键词">
		<meta name="Description" content="描述">
		<title>腾讯空间换肤</title>
		<!-- css js-->
		<style>
		/*css语法    选择器{样式属性：值；样式属性：值；}*/
		*{margin:0;padding:0;}
		body{/*元素选择器 标签名*/
			background-color:#000;
			background-image:url('images/b1.jpg');
			background-repeat:no-repeat;
			background-position:center top;
		}
		.bg-nav{/*类选择器 以class命名*/
			width:900px;
			height:120px;
			background:rgba(255,255,255,0.5);
			margin:300px auto 0;/*上外边距 左右居中 下*/
			position:relative;
			padding:10px 0;
		}
		.bg-nav .pic{/*后代选择器*/
			width:844px;
			height:120px;
			margin:0 auto;/*上下 左右*/
			overflow:hidden;
			position:relative;/*相对定位 参照物*/
		}
		.bg-nav .pic ul{
			width:300%;
			height:120px;
			position:absolute;/*绝对定位*/
			left:0;top:0;
		}
		.bg-nav .pic ul li{
			width:175px;
			height:110px;
			list-style:none;
			float:left;/*左浮动*/
			border:5px solid #fff;
			margin:0 13px;
		}
		.bg-nav img.btn{
			position:absolute;
			top:55px;
		}
		.bg-nav .left{
			left:15px;
		}
		.bg-nav .right{
			right:15px;
		}
		</style>
	</head>
	<body>
		<div class="bg-nav">
			<div class="pic">
				<ul>
					<li>
					<img src="images/s1.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s2.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s3.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s4.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s5.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s6.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s7.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s8.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s9.jpg" width="175" height="110" alt=""/>
					</li>
					<li>
					<img src="images/s10.jpg" width="175" height="110" alt=""/>
					</li>
				</ul>
			</div>
			<img class="btn left" src="images/dirl.png">
			<img class="btn right" src="images/dirr.png">
		</div>
	</body>
</html>
<script src="js/jquery.js"></script>
<script>
	var num = 0;
	$('.bg-nav .left').click(function(){
		num++;
		if(num>2){
			num = 2;
			alert('已经到头了，不能在移动了');
		}
		$('ul').animate({left:-844*num+'px'},500);
	});
	$('.bg-nav .right').click(function(){
		num--;
		if(num<0){
			num = 0;
			alert('已经到头了，不能在移动了');
		}
		$('ul').animate({left:-844*num+'px'},500);
	});
	//换肤
	var arr = ['b1.jpg','b2.jpg','b3.jpg','b4.jpg','b5.jpg','b6.jpg','b7.jpg','b8.jpg','b9.jpg','b10.jpg'];
	$('.bg-nav .pic ul li').click(function(){
		var i = $(this).index();//当前序列
		$('body').css({'background-image':"url('images/"+arr[i]+"')"})
	})
</script>

```

