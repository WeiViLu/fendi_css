# 图片收缩，边框收缩效果<br />
# 图片收缩<br />
&nbsp; 通过设置盒子大小，图片位置，隐藏图片的一部分，达到鼠标移上去有图片向后移的效果。css部分如下：&lt;br&gt;<br />
&nbsp; <span style="white-space:pre">	</span> &nbsp;```<br />
<span style="white-space:pre">		</span>.box{<br />
<span style="white-space:pre">			</span>width: 405px;<br />
<span style="white-space:pre">			</span>height: 216px;<br />
<span style="white-space:pre">			</span>overflow: hidden;<br />
<span style="white-space:pre">			</span>position: relative;<br />
<span style="white-space:pre">			</span>margin: 0 auto;<br />
<span style="white-space:pre">			</span>margin-top: 50px;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.box:hover .inn{<br />
<span style="white-space:pre">			</span>transform: scale(0.9);<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.inn{<br />
<span style="white-space:pre">			</span>position: absolute;<br />
<span style="white-space:pre">			</span>top: -12px;<br />
<span style="white-space:pre">			</span>left:-25px;<br />
<span style="white-space:pre">			</span>transition:0.5s;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">	</span> &nbsp;```<br />
# 边框收缩效果<br />
&nbsp; 在盒子里放四个div，代表盒子的四条边。html部分如下：&lt;br&gt;<br />
&nbsp; <span style="white-space:pre">		</span>```<br />
<span style="white-space:pre">		</span>&lt;div class=&quot;box&quot;&gt;<br />
<span style="white-space:pre">			</span>&lt;img src=&quot;http://www.fendi.cn//sites/all/themes/fendi/img/homepage/170629/b-455-240.jpg&quot; alt=&quot;&quot; class=&quot;inn&quot;&gt;<br />
<span style="white-space:pre">			</span>&lt;div class=&quot;line-left&quot;&gt;&lt;/div&gt;<br />
<span style="white-space:pre">			</span>&lt;div class=&quot;line-top&quot;&gt;&lt;/div&gt;<br />
<span style="white-space:pre">			</span>&lt;div class=&quot;line-right&quot;&gt;&lt;/div&gt;<br />
<span style="white-space:pre">			</span>&lt;div class=&quot;line-bottom&quot;&gt;&lt;/div&gt;<br />
<span style="white-space:pre">		</span>&lt;/div&gt;<br />
<span style="white-space:pre">		</span>```<br />
&nbsp;设置四条边的位置：&lt;\br&gt;<br />
&nbsp; &nbsp;<span style="white-space:pre">	</span> &nbsp; &nbsp; &nbsp;```<br />
<span style="white-space:pre">		</span>.line-left,.line-right,.line-top,.line-bottom{<br />
<span style="white-space:pre">			</span>transition: 0.8s ease-out;／／缓慢消失<br />
<span style="white-space:pre">			</span>position: absolute;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-left,.line-right{<br />
<span style="white-space:pre">			</span>height: 216px;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-top,.line-bottom{<br />
<span style="white-space:pre">			</span>width: 405px;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-left{<br />
<span style="white-space:pre">			</span>border-left:2px solid gold;<br />
<span style="white-space:pre">			</span>left: 0px;<br />
<span style="white-space:pre">			</span>bottom: 0;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-right{<br />
<span style="white-space:pre">			</span>border-right:2px solid gold;<br />
<span style="white-space:pre">			</span>right: 0px;<br />
<span style="white-space:pre">			</span>bottom: 0;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-top{<br />
<span style="white-space:pre">			</span>border-top: 2px solid gold;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.line-bottom{<br />
<span style="white-space:pre">			</span>border-bottom: 2px solid gold;<br />
<span style="white-space:pre">			</span>left: 0;<br />
<span style="white-space:pre">			</span>bottom: 0;<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>动画效果：<br />
<span style="white-space:pre">		</span>.box:hover .line-left{<br />
<span style="white-space:pre">			</span>transform: translateY(-100%);<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.box:hover .line-right{<br />
<span style="white-space:pre">			</span>transform: translateY(100%);<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.box:hover .line-top{<br />
<span style="white-space:pre">			</span>transform: translateX(-100%);<br />
<span style="white-space:pre">		</span>}<br />
<span style="white-space:pre">		</span>.box:hover .line-bottom{<br />
<span style="white-space:pre">			</span>transform: translateX(100%);<br />
<span style="white-space:pre">		</span>}<br />
&nbsp; &nbsp; <span style="white-space:pre">	</span> &nbsp; &nbsp;```<br />
&nbsp; &nbsp;&nbsp;
