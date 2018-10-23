###表单、表格
####表单
######表单的作用
表单通常是用于需要收集用户输入的一些数据时，比如用户名密码、性别选项等等的时候。
######表单的结构
表单的构成为一个表单区域（form）和若干表单元素（input）
**表单区域：**规定一个表单的范围，以及提交的地址方式等等，
**表单元素：**用于收集具体数据的标签元素，有许多不同的类型，主要学的是表单元素的功能。
***
####<form>
```
<form action="" method="">
   <ul>
    <li>
      <input type="text" name="" />
  </li>
</ul>
</form>
```
####概述
**HTML <form> 元素** 表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。
可以用 [`:valid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:valid ":valid CSS 伪类表示内容验证正确的<input> 或其他 <form> 元素。这能简单地将校验字段展示为一种能让用户辨别出其输入数据的正确性的样式。") 和[`:invalid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:invalid "此页面仍未被本地化, 期待您的翻译!") CSS 伪类 来给一个元素指定样式。
####属性
**action**提交地址   
值：URL
这个值可以被 [`<button>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button "HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。") 或者 [`<input>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input "HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。") 元素中的 [`formaction`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button#attr-formaction) 属性重载（覆盖）。

**method** 提交的方式
`get `：普通提交方式
`post` ：加密提交方式
*   `post`: 指的是 HTTP [post方法](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.5 "http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.5") ; 表单数据会包含在表单体内然后发送给服务器.
*   `get`: 指的是 HTTP [get方法](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.3 "http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.3"); 表单数据会附加在 `action` 属性的URI中，并以 '?' 作为分隔符, 然后这样得到的 URI 再发送给服务器. 当这样做（数据暴露在URI里面）没什么副作用，或者表单仅包含ASCII字符时，再使用这种方法吧。

这个值可以被 [`<button>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button "HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。") 或者 [`<input>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input "HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。") 元素中的 [`formmethod`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button#attr-formmethod)属性重载（覆盖）。


**autocapitalize**

这是一个被 iOS Safari Mobile 使用的非标准属性。当用户在一些form的文本后代控件中，输入/编辑一些文本值时，这个属性控制了是否和怎样，对这些文本值首字母大写化。如果**autocapitalize**属性在某个单独的form后代控件被指定的话，那么这个单独的设定会干掉（原先）form范围内的 autocapitalize 设定. 这个非不推荐的值从 iOS 5 及其之后可用. 默认值为 sentences. 可以选择的值如下:
* `none`: 完全禁用自动首字母大写.
* `sentences`: 自动对每句话首字母大写.
* `words`: 自动对每个单词首字母大写.
* `characters`: 自动大写所有的字母.

**autocomplete**

用于指示 input 元素是否能够拥有一个默认值，这个默认值是由浏览器自动补全的。这个设定可以被属于这个form的子元素的 `autocomplete` 属性重载（覆盖）。 可能的值有:

*   `off`: 在每一个用到的输入域里，用户必须显式的输入一个值，或者document 以它自己的方式提供自动补全；浏览器不会自动补全输入。
*   `on`: 浏览器能够根据用户之前在form里输入的值自动补全。
**`注意`**
`如果你在一个表单里把 `autocomplete` 设置成 `off` 是因为 document 提供了它独有的自动补全，那么你也应该把这个表单里每一个 input 元素的 `autocomplete` 设成 `off` 来让 document 能够自动补全.` 想要了解详细信息, 参见 [Google Chrome notes](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/form#Google_Chrome_notes).

**enctype**

当 **method** 属性值为 `post` 时,` enctype` 是提交form给服务器的内容的 MIME 类型 。可能的取值有:
* `application/x-www-form-urlencoded`: 如果属性未指定时的默认值。
* `multipart/form-data`: 这个值用于一个 type 属性设置为 `"file"` 的 **<input>** 元素。
* `text/plain`

这个值可以被 [`<button>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button "HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。") 或者 [`<input>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input "HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。") 元素中的 [formenctype](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button#attr-formenctype)属性重载（覆盖）。



**novalidate**

这个布尔类型的属性指示了，当提交时form是否没有被验证。 如果这个属性没有指定 (因此这个 form 是验证通过的)，这个默认设置可以被属于这个form的 [`<button>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button "HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。") 或者 [`<input>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input "HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。") 元素中的 [formnovalidate](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button#attr-formnovalidate)属性重载（覆盖）。

**target**

一个名字或者说关键字，用来指示在提交表单之后，在哪里显示收到的回复. 在 HTML 4 里, 这是一个用于 frame 的名字/关键字. 在 HTML5 里, 这是一个用于 **browsing context 浏览器上下文** 的名字/关键字 (举例来说, 标签页tab, 窗口window, or 或者行内 frame). 如下的关键字含有特别的含义:

*   `_self`: 在当前HTML4或HTML5文档页面重新加载返回值。这个是默认值。**译注：也就是说如果这个文档在一个frame中的话，self是在当前frame（document）中重新加载的，而不是整个页面（window）。**
*   `_blank`: 以新的HTML4或HTML5文档窗口加载返回值。
*   `_parent`: 在父级的frame中以HTML4或HTML5文档形式加载返回值，如果没有父级的frame，行为和_self一致。
*   `_top`: 如果是HTML 4文档: 清空当前文档，加载返回内容；HTML5: 在当前文档的最高级内加载返回值，如果没有父级，和_self的行为一致。
*   **iframename**: 返回值在指定frame中加载。

HTML5: 这个值可以被 [`<button>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button "HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。") 或者 [`<input>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input "HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。") 元素中的 [formtarget](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button#attr-formtarget)属性重载（覆盖）。

**例子**
```<!-- 一个简单的表单，这个表单会发送一个 GET 请求 -->
<form action="">
  <label for="GET-name">Name:</label>
  <input id="GET-name" type="text" name="name">
  <input type="submit" value="Save">
</form>

<!-- 一个简单的表单，发送 POST 请求 -->
<form action="" method="post">
  <label for="POST-name">Name:</label>
  <input id="POST-name" type="text" name="name">
  <input type="submit" value="Save">
</form>

<!-- 使用 fieldset, legend, and label 的表单 -->
<form action="" method="post">
  <fieldset>
    <legend>Title</legend>
    <input type="radio" name="radio" id="radio"> <label for="radio">Click me</label>
  </fieldset>
</form>
```

#####表单元素属性
* **name**
指定表单元素的名字，对表单元素进行标识，与value属性的值进行对应。
* **value**
value属性的值表示，收集并且需要发送数据值，可以主动设置，但大多数是用户动态进行修改的。
#####<input>
input是from表单里的一个表单项，可以通过不同的`type`值成为不同作用的表单元素
```
<input typle="text" value=""  name="usersname" />
```
**input的type属性值**
* `text` 单行文本输入框
* `password` 加密文本输入框
* `radio` 单选框
* `checkbox` 多选框
* `submit` 提交按钮
* `button` 普通按钮
* `reset` 重置按钮
* `hidden` 隐藏输入框
* `file` 文本选择框
* `date` 日期控件  
* `color` 颜色控件

####textarea
`多行文本框`

**功能**：创建一个多行文本输入框
**属性**：
`cols`：规定一行文本输入的最大字节（不标准）
`rows`：规定输入文本最大显示行数
**`css属性`**：
`resize:none;`  禁止改变大小

####select>option
`下拉列表`
一种表单控件，可用于在表单中接受用户输入。

**功能**：创建一个下拉列表
**属性**：
`cols`：规定一行文本输入的最大字节（不标准）
`rows`：规定输入文本最大显示行数
`mutiple`：规定可以选择多个项
**`css属性`**：
`resize:none;`  禁止改变大小
**结构展示**
```
<select id="pet-select">
    <option value="">--Please choose an option--</option>
    <option value="dog">Dog</option>
    <option value="cat">Cat</option>
    <option value="hamster">Hamster</option>
    <option value="parrot">Parrot</option>
    <option value="spider">Spider</option>
    <option value="goldfish">Goldfish</option>
</select>
```
####特殊表单属性

* `checked`：默认选中该表单元素，用于单选框或者多选框
* `placeholder`：规定元素中默认显示的提示的内容，用于文本输入框
* `autofocus`：光标默认选中，用于文本输入框

####lable标签
通过lable标签的for属性可以关联标记某些表单元素，使用户在使用鼠标操作时更加方便
```
<form action=””>

    <input type=”text”  value=”” id=”textID” />
    <label for=”textID”>点击输入文本</label>

    <input type=”checkbox”  value=”” id=”checkboxID”  />
    <label for=”radioID”>点击选中复选框</label>

</form>
```

###表格
####概述
表格主要由单元格（td）和表格行（tr）组成，一个代表列，一个代表行，整体放在一个table标签内。表格的表现看起来就是排列整齐的盒子，只有些许多不同的宽高特性

**示例代码结构**：
```
<table border="1">
    <thead>
        <tr><th colspan="4">食物表</th></tr>
    </thead>
    <tbody>
        <tr><th>水果</th><th>蔬菜</th><th>主食</th><th>调料</th></tr>
        <tr><td>苹果</td><td>白菜</td><td>大米</td><td>辣椒</td></tr>
        <tr><td>香蕉</td><td>青菜</td><td>小麦</td><td>大葱</td></tr>
    </tbody>
    <tfoot>
        <tr><th>备注</th><td  colspan="3"></td></tr>
     </tfoot>
</table>	
```
####表格的属性
1. 表格边框属性
    <table border='1'></table>
2. 边框合并样式
    table{ border-collapse:collapse; }
3. 单元格合并行属性
    <td rowspan='2'><td>
4. 单元格合并列属性
    <td colspan='3'><td>

####表格的特性
表格的一些宽度高度，以及文字等等的特性，而且表格的特性比较怪异
####表格的属性
1. 单元格默认会以内容多少为参考，按百分比分配table 的宽度
2. 表格同一列 / 行的宽度 / 高度会和该行 / 列的最大的单元格一致
3. th里面的内容默认加粗并且左右上下居中
4. td里面的内容默认上下居中 左对齐显示
5. th,td设置margin时没有效果