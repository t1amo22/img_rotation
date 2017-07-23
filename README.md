# img_rotation
<h4>1.html、css</h4>
<ul>
<li>放置图片顺序为 5 12345 1，可实现无缝轮播，外层为container，内层有wrap放置图片，buttons放置按钮，两个a标签是左右的箭头</li>
<li>最外层container元素宽度600px,height400px，和图片设置成大小一样，相对定位，overflow设置为hidden</li>
<li>wrap的宽度为所有图片宽度的总和，绝对定位，并设置行内样式left为-600px.即可显示第一张图片</li>
<li>buttons和箭头均绝对定位</li>
</ul>
<h4>2.功能</h4>
<h5>1）左右选择功能</h5>
<p>给每个箭头添加click事件，单击后获取到left值，先判断是否为边界值（右边边界是-3600，左边是0），如果是边界值将其设置为newleft(右边第二张-1200，左边第四张-2400)</p>
<h5>2）下标关联功能</h5>
<p>设置初始的index是0.点击左右箭头后让index++/--,边界值index&gt;4的时候为0，index&lt;0的时候为4，然后执行函数changedot(index),获取到span的nodelist，首先清空所有span的class，然后设置span[i]的class为&ldquo;on&rdquo;</p>
<h5>3）自动播放功能</h5>
<p>设置一个timer，fn函数为next_pic(),</p>
<h5>4)鼠标悬浮时停止播放，移出时自动播放</h5>
<p>给container添加mouseenter事件，clearInterval(timer)，mouseleave事件autoplay()</p>
<h5>5)点击button按钮切换图片</h5>
<p>使用事件委托给span绑定事件，获取到innerHTML,然后改变class，使用switch语句切换wrap的left值</p>


