如果出了问题，搞一个初始动画

首先，我们需要设置一套 HTML 和 CSS

index.html

```HTML
<div class="NavigationView">

</div>
<div class="Windows">

</div>
```

WinXUI.css

```CSS
/*
你想想看每个文字标题行都有特定的样式
遵照微软设计多好
*/

:root {
	--tizi:
	--daxiao:
}

.NavigationView {
/*总之是所有界面的基础*/
/*甚至可以加点媒体查询*/
} 
.Windows {
/*基！础！*/
/*媒体查询找微软！*/
}
```

现在我们有了这样一套东西，如何干好事呢？

例如 NavigationView.css

```CSS
.NavigationView > ul {
/*好东西*/
}

.NavigationView > li {
/*话说这是不是初始就应该有的*/
}
```

NavigationView.js

```JS
function ul(ull,img){
	let ulll = document.querySelector('img');
	let ulll = document.querySelector('ul');
	ul.textContent = ull
	document.createTextNode
}

function li(lii,img){
	let liii = document.querySelector('img');
	let liii = document.querySelector('li');
	li.textContent = lii
	document.createTextNode
}
```

当然了二十四小时常驻就别丢人现眼了，直接直接写 HTML 里得了

我们还有自定义模块

例如 Windows.css

```CSS
.box {
/*好东西*/
}
```

Windows.js

```JS
function box(ull,img){
	let ulll = document.querySelector('img');
	let ulll = document.querySelector('ul');
	ul.textContent = ull
	document.createTextNode
}
```

我们详细讨论一下

## 讨！论！

我们有

WinXUI.css

在这个文件里，注册我们的基础盒子

TitleBar

NavigationView

Windows

像这样

TitleBar.img = 

NavigationView.list(dt,dd)

Windows.box(img,name,following,followers)

一个 HTML 应该长这样

```HTML
<div class="NavigationView">
	<div class="listBox">
		<dl class="list">
			<dt>apple</dt>
			<dd>apple</dd>
			<dd>apple</dd>
		</dl>
		<dl class="list">
			<dt>apple</dt>
			<dd>apple</dd>
			<dd>apple</dd>
		</dl>
		<dl class="list">
			<dt>apple</dt>
			<dd>apple</dd>
			<dd>apple</dd>
		</dl>
	</div>
	<div class="listxBox">
		<ul class="listX">
			<li>apple</li>
			<li>apple</li>
			<li>apple</li>
		</ul>
	</div>
</div>
```

不妨这样

```HTML
<基础盒子>
	<命令盒子>
		<排版盒子>
			<组件盒子>
			</组件盒子>
			<组件盒子>
			</组件盒子>
			<组件盒子>
			</组件盒子>
		</排版盒子>
	</命令盒子>
</基础盒子>
```

我们的排版盒子不仅排版“组件盒子”，还参与到排版当中去

基础盒子是万不能动的！如果要排版”排版盒子“需要借助”置新盒子“

其中，排版“排版盒子”的盒子就是“置新盒子”

而我们的基础盒子就是注册的那几个

TitleBar.img = 

NavigationView.list(dt,dd)

Windows.box(img,name,following,followers)

有事件了！

```
doc.id(id,"")
this.id
```

给大家看个好东西

```JS
btn.onclick = function() {
	packing("NavigationView",)
}
```

```JS
funtcion packing(cmd,id,oid)
let nev = cmd.packing
let too = document.getElementById(id);
let old = document.getElementById(oid);

too.replaceChild(cmd,old);
```

```JS
function pacmd(img,name,following,followers){
	let cmd = document.createElement('div');
	
	let cmdImg = document.createElement('img');
	cmdImg.setAttribute("src",img);
	cmd.appendChild(cmdImg)
	
	let cmdName = document.createElement('p');
	cmdName.textContent = name;
	cmd.appendChild(cmdName)
	
	let cmdFollowing = document.createElement('span');
	cmdFollowing.textContent = following + "关注";
	cmd.appendChild(cmdFollowing)
	
	let cmdFollowers = document.createElement('span');
	cmdFollowers.textContent = followers + "粉丝";
	cmd.appendChild(cmdFollowers)
	
	retrun cmd
}
```

## 最终决定

万物皆是组件

那就是

widgets

packages

windows

个人资料卡片

widget.profileCard(img,name,following,followers)

## 最终决定

我们有同步文件夹 Git

我们需要将我们的包丢进去进行同步，推送至存储库

然后如果你写包写不解恨还可以写函数，多好

### 包

我们的包只需要给一个数组就能运行

```
npm.option()
npm.musicList()
npm.profileCard()
```

让我们看看我们的包都写了些什么

```

```

```JS
funtcion push(cmd,id,oid)
let too = document.getElementById(id);
let old = document.getElementById(oid);

too.replaceChild(cmd,old);
```

然后我们的事件

```JS
potato.onclick = git.potato(Array)
```

你说浪费了？不不不，如果按原来我们还要写一个 `retrun` 语句，而现在原来的位置写着 `push`，而我们本来也要运行 `push` 函数，不仅没少写行数，甚至还少了一步 `retrun`，代码也更好理解了，现在我们仅需在事件处填入数组就可以了！

### 函数

不妨看看组件

```HTML

```

### 控件

绝对位置和相对位置

他的控件是控件，我的是......

所谓控件是基于我们的东西起的名字，吧

我们都知道，是个人都知道，我们的选项是构建出来的

```JS
let cmdName = document.createElement('p');
cmdName.onclick = git[json.name](json.todo);
```

那就只剩下一个未解决了

### 相对选择器

有异步么？

控件是不是只有一个地方有？

示例

```JS
apple.addEventListener('click', event => git.apple(event,Array));
```

```JS
git.apple = function(e,ar){
	//..........................
	e.target.parentNode.replaceChild(cmd,e.target);
}
```

这串代码相当于 Push 函数

这个，自动化基础，数组加检测个数循环！

我们还有括号表示法，前途一片光明啊！

# 可以只送数组搞合并

# 然后现在去按正轨吧，按实践正轨

这个 表单放在 HTML CSS JS 结合 之际

JS

HTML

HTML JS（Web API）

CSS（动画）

CSS JS（肯定有一些HTML，过渡嘛）（Web API）

HTML CSS JS（表单！）（Web API）

Web API（事件！）