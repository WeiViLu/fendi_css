# 图片收缩，边框收缩效果
# 图片收缩
  通过设置盒子大小，图片位置，隐藏图片的一部分，达到鼠标移上去有图片向后移的效果。css部分如下：<br>
``` bash
	.box{
		width: 405px;
		height: 216px;
		overflow: hidden;
		position: relative;
		margin: 0 auto;
		margin-top: 50px;
	}
	.box:hover .inn{
		transform: scale(0.9);
	}
	.inn{
		position: absolute;
		top: -12px;
		left:-25px;
		transition:0.5s;
	}
```
# 边框收缩效果
  在盒子里放四个div，代表盒子的四条边。html部分如下：<br>
``` bash
		<div class="box">
			<img src="http://www.fendi.cn//sites/all/themes/fendi/img/homepage/170629/b-455-240.jpg" alt="" class="inn">
			<div class="line-left"></div>
			<div class="line-top"></div>
			<div class="line-right"></div>
			<div class="line-bottom"></div>
		</div>
```
 设置四条边的位置：<br>
``` bash
		.line-left,.line-right,.line-top,.line-bottom{
			transition: 0.8s ease-out;／／缓慢消失
			position: absolute;
		}
		.line-left,.line-right{
			height: 216px;
		}
		.line-top,.line-bottom{
			width: 405px;
		}
		.line-left{
			border-left:2px solid gold;
			left: 0px;
			bottom: 0;
		}
		.line-right{
			border-right:2px solid gold;
			right: 0px;
			bottom: 0;
		}
		.line-top{
			border-top: 2px solid gold;
		}
		.line-bottom{
			border-bottom: 2px solid gold;
			left: 0;
			bottom: 0;
		}
		动画效果：
		.box:hover .line-left{
			transform: translateY(-100%);
		}
		.box:hover .line-right{
			transform: translateY(100%);
		}
		.box:hover .line-top{
			transform: translateX(-100%);
		}
		.box:hover .line-bottom{
			transform: translateX(100%);
		}
```
    
