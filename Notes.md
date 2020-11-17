# Chart

[『Cmd 技术渲染的沙箱页面，点击此处编写自己的文档』](https://www.zybuluo.com/mdeditor "作业部落旗下 Cmd 在线 Markdown 编辑阅读器")

# Cmd Markdown 简明语法手册

标签： Cmd-Markdown

---

### 1. 斜体和粗体

使用 * 和 ** 表示斜体和粗体。

示例：

这是 *斜体*，这是 **粗体**。

### 2. 分级标题

使用 === 表示一级标题，使用 --- 表示二级标题。

示例：

```
这是一个一级标题
============================

这是一个二级标题
--------------------------------------------------

### 这是一个三级标题
```

你也可以选择在行首加井号表示不同级别的标题 (H1-H6)，例如：# H1, ## H2, ### H3，#### H4。

### 3. 外链接

使用 \[描述](链接地址) 为文字增加外链接。

示例：

这是去往 [本人博客](http://ghosertblog.github.com) 的链接。

### 4. 无序列表

使用 *，+，- 表示无序列表。

示例：

- 无序列表项 一
- 无序列表项 二
- 无序列表项 三

### 5. 有序列表

使用数字和点表示有序列表。

示例：

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

### 6. 文字引用

使用 > 表示文字引用。

示例：

> 野火烧不尽，春风吹又生。

### 7. 行内代码块

使用 \`代码` 表示行内代码块。

示例：

让我们聊聊 `html`。

### 8.  代码块

使用 四个缩进空格 表示代码块。

示例：

    这是一个代码块，此行左侧有四个不可见的空格。

### 9.  插入图像

使用 \!\[描述](图片链接地址) 插入图像。

示例：

![我的头像](https://www.zybuluo.com/static/img/my_head.jpg)

# Cmd Markdown 高阶语法手册

### 1. 内容目录

在段落中填写 `[TOC]` 以显示全文内容的目录结构。

[TOC]

### 2. 标签分类

在编辑区任意行的列首位置输入以下代码给文稿标签：

标签： 数学 英语 Markdown

或者

Tags： 数学 英语 Markdown

### 3. 删除线

使用 ~~ 表示删除线。

~~这是一段错误的文本。~~

### 4. 注脚

使用 [^keyword] 表示注脚。

这是一个注脚[^footnote]的样例。

这是第二个注脚[^footnote2]的样例。

### 5. LaTeX 公式

$ 表示行内公式： 

质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。

$$ 表示整行公式：

$$\sum_{i=1}^n a_i=0$$

$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$

$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$

访问 [MathJax](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) 参考更多使用方法。

### 6. 加强的代码块

支持四十一种编程语言的语法高亮的显示，行号显示。

非代码示例：

```
$ sudo apt-get install vim-gnome
```

Python 示例：

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

JavaScript 示例：

``` javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}

document.write(fib(10));
```

### 7. 流程图

#### 示例

```flow
st=>start: Start:>https://www.zybuluo.com
io=>inputoutput: verification
op=>operation: Your Operation
cond=>condition: Yes or No?
sub=>subroutine: Your Subroutine
e=>end

st->io->op->cond
cond(yes)->e
cond(no)->sub->io
```

#### 更多语法参考：[流程图语法参考](http://adrai.github.io/flowchart.js/)

### 8. 序列图

#### 示例 1

```seq
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

#### 示例 2

```seq
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

#### 更多语法参考：[序列图语法参考](http://bramp.github.io/js-sequence-diagrams/)

### 9. 甘特图

甘特图内在思想简单。基本是一条线条图，横轴表示时间，纵轴表示活动（项目），线条表示在整个期间上计划和实际的活动完成情况。它直观地表明任务计划在什么时候进行，及实际进展与计划要求的对比。

```gantt
    title 项目开发流程
    section 项目确定
        需求分析       :a1, 2016-06-22, 3d
        可行性报告     :after a1, 5d
        概念验证       : 5d
    section 项目实施
        概要设计      :2016-07-05  , 5d
        详细设计      :2016-07-08, 10d
        编码          :2016-07-15, 10d
        测试          :2016-07-22, 5d
    section 发布验收
        发布: 2d
        验收: 3d
```

#### 更多语法参考：[甘特图语法参考](https://knsv.github.io/mermaid/#gant-diagrams)

### 10. Mermaid 流程图

```graphLR
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

#### 更多语法参考：[Mermaid 流程图语法参考](https://knsv.github.io/mermaid/#flowcharts-basic-syntax)

### 11. Mermaid 序列图

```sequence
    Alice->John: Hello John, how are you?
    loop every minute
        John-->Alice: Great!
    end
```

#### 更多语法参考：[Mermaid 序列图语法参考](https://knsv.github.io/mermaid/#sequence-diagrams)

### 12. 表格支持

| 项目   |   价格 | 数量 |
| ------ | -----: | :--: |
| 计算机 | \$1600 |  5   |
| 手机   |   \$12 |  12  |
| 管线   |    \$1 | 234  |


### 13. 定义型列表

名词 1
:   定义 1（左侧有一个可见的冒号和四个不可见的空格）

代码块 2
:   这是代码块的定义（左侧有一个可见的冒号和四个不可见的空格）

        代码块（左侧有八个不可见的空格）

### 14. Html 标签

本站支持在 Markdown 语法中嵌套 Html 标签，譬如，你可以用 Html 写一个纵跨两行的表格：

    <table>
        <tr>
            <th rowspan="2">值班人员</th>
            <th>星期一</th>
            <th>星期二</th>
            <th>星期三</th>
        </tr>
        <tr>
            <td>李强</td>
            <td>张明</td>
            <td>王平</td>
        </tr>
    </table>


<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>

### 15. 内嵌图标

本站的图标系统对外开放，在文档中输入

    <i class="icon-weibo"></i>

即显示微博的图标： <i class="icon-weibo icon-2x"></i>

替换 上述 `i 标签` 内的 `icon-weibo` 以显示不同的图标，例如：

    <i class="icon-renren"></i>

即显示人人的图标： <i class="icon-renren icon-2x"></i>

更多的图标和玩法可以参看 [font-awesome](http://fortawesome.github.io/Font-Awesome/3.2.1/icons/) 官方网站。

### 16. 待办事宜 Todo 列表

使用带有 [ ] 或 [x] （未完成或已完成）项的列表语法撰写一个待办事宜列表，并且支持子列表嵌套以及混用Markdown语法，例如：

    - [ ] **Cmd Markdown 开发**
        - [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
        - [ ] 支持以 PDF 格式导出文稿
        - [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
        - [x] 改进 LaTex 功能
            - [x] 修复 LaTex 公式渲染问题
            - [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
    - [ ] **七月旅行准备**
        - [ ] 准备邮轮上需要携带的物品
        - [ ] 浏览日本免税店的物品
        - [x] 购买蓝宝石公主号七月一日的船票

对应显示如下待办事宜 Todo 列表：
        
- [ ] **Cmd Markdown 开发**
    - [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
    - [ ] 支持以 PDF 格式导出文稿
    - [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
    - [x] 改进 LaTex 功能
        - [x] 修复 LaTex 公式渲染问题
        - [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
- [ ] **七月旅行准备**
    - [ ] 准备邮轮上需要携带的物品
    - [ ] 浏览日本免税店的物品
    - [x] 购买蓝宝石公主号七月一日的船票
      
        
[^footnote]: 这是一个 *注脚* 的 **文本**。

[^footnote2]: 这是另一个 *注脚* 的 **文本**。

# 替换

1. '^'→'#'
2. '@'→'^'

# Shotcut



[![img](https://img2018.cnblogs.com/blog/443934/201810/443934-20181012170159282-378811511.png)](https://img2018.cnblogs.com/blog/443934/201810/443934-20181012170159282-378811511.png)

[![img](https://img2018.cnblogs.com/blog/443934/201810/443934-20181012170211920-1988294604.png)](https://img2018.cnblogs.com/blog/443934/201810/443934-20181012170211920-1988294604.png)



## 一：菜单栏



- 文件：alt+F
- 编辑：alt+E
- 段落：alt+P
- 格式：alt+O
- 视图：alt+V
- 主题：alt+T
- 帮助：alt+H



## 二：文件



- 新建：Ctrl+N
- 新建窗口：Ctrl+Shift+N
- 打开：Ctrl+O
- 快速打开：Ctrl+P
- 保存：Ctrl+S
- 另存为：Ctrl+Shift+S
- 偏好：Ctrl+,
- 关闭：Ctrl+W



## 三：编辑



- 撤销：Ctrl+Z
- 重做：Ctrl+Y
- 剪切：Ctrl+X
- 复制：Ctrl+C
- 粘贴：Ctrl+V
- 复制为MarkDown：Ctrl+Shift+C
- 粘贴为纯文本：Ctrl+Shift+V
- 全选：Ctrl+A
- 选中当前行/句：Ctrl+L
- 选中当前格式文本：Ctrl+E
- 选中当前词：Ctrl+D
- 跳转到文首：Ctrl+Home
- 跳转到所选内容：Ctrl+J
- 跳转到文末：Ctrl+End
- 查找：Ctrl+F
- 查找下一个：F3
- 查找上一个：Shift+F3
- 替换：Ctrl+H



## 四：段落



- 标题：Ctrl+1/2/3/4/5
- 段落：Ctrl+0
- 增大标题级别：Ctrl+=
- 减少标题级别：Ctrl+-
- 表格：Ctrl+T
- 代码块：Ctrl+Shift+K
- 公式块：Ctrl+Shift+M
- 引用：Ctrl+Shift+Q
- 有序列表：Ctrl+Shift+[
- 无序列表：Ctrl+Shift+]
- 增加缩进：Ctrl+]
- 减少缩进：Ctrl+[



## 五：格式



- 加粗：Ctrl+B
- 斜体：Ctrl+I
- 下划线：Ctrl+U
- 代码：Ctrl+Shift+`
- 删除线：Alt+Shift+5
- 超链接：Ctrl+K
- 图像：Ctrl+Shift+I
- 清除样式：Ctrl+



## 六：视图



- 显示隐藏侧边栏：Ctrl+Shift+L
- 大纲视图：Ctrl+Shift+1
- 文档列表视图：Ctrl+Shift+2
- 文件树视图：Ctrl+Shift+3
- 源代码模式：Ctrl+/
- 专注模式：F8
- 打字机模式：F9
- 切换全屏：F11
- 实际大小：Ctrl+Shift+0
- 放大：Ctrl+Shift+=
- 缩小：Ctrl+Shift+-
- 应用内窗口切换：Ctrl+Tab
- 打开DevTools：Shift+F12

# 文字题整理版式

1. 名词解释：每个名词分为两行，第一行为名词及外文翻译，第二行为解释（信息量过大时，接受换行，但不得换段）。两个名词解释间为换段，不为换行。
2. 叙述题内小标题需用斜体加粗，文段内重点使用字体加黑加粗。
3. 每小题内最多有一个等级的列表，不能过多。

# 希腊字母

α　Α　alpha /alpha/ h表示送气音，在古希腊语中尚没有音位/f/，所以/pha/的发音类似普通话的“趴”。
β　Β　beta /be:ta/ /e:/表示长元音，/e/的发音不是英语D.J.音标里的[e]，而类似K.K.音标里的/e/或者法语的/e/。/t/不送气，所以/ta/类似普通话“搭”而不是“他”。
γ　Γ　gamma /gam:a/　/m:/表示长辅音，即在发辅音时，其持阻阶段应该适当延长，然后再做除阻动作。
δ　Δ　delta /de:lta/
ε　Ε　epsilon /epsilo:n/ /o/的发音要比英国英语字母组合au的发音更闭一些。
ζ　Ζ　zeta /ze:ta, dze:ta/ /z, dz/浊的塞音或塞擦音。
η　Η　eta /e:ta/ 第一个音节为长音。
θ　Θ　theta /the:ta/ /th/表示送气音，t为齿化的(dentalised)塞音，而不是英语里的/t/，类似汉语里的t，但要更紧一些。
ι　Ι　iota /jo:ta，io:ta/
κ　Κ　kappa /kap:a/ /p:/表示长辅音，其描述类似/m:/，前一个p类似于英语里“失去爆破”或者汉语粤方言中的塞音韵尾/-p/，/k/不送气。
λ　Λ　lambda /lambda/
μ　Μ　my /my:/ /y:/是长元音，类似汉语的“淤”以及法语字母u单独存在时的发音。
ν　Ν　ny /ny:/
ξ　Ξ　xi /ksi:/
ο　Ο　omicron /omikro:n/ micron表示“小”，所以是“短o”的意思。
π　Π　pi /pi:/ /p/不送气，所以应该类似“逼”而不是“批”。
ρ　Ρ　rho /rho:/ /rh/实际上表示清化的擦颤音，这里打不出来，姑且用这个组合吧。据说捷克语里有，这就是为什么Dvorak被翻译为“德沃夏克”而不是“德沃拉克”的原因。据说古希腊语有两个颤音，一个是词头的擦颤音，一个是词尾的成音节的真正浊颤音，所以希腊字母标里有两个rho，一个只用在词头，一个只用在词尾。
σ　Σ　sigma /sigma/ /s/为齿化的，类似汉语的s-，而不是英语的[s]。与rho类似希腊字母表里也有两个sigma，一个在词头，一个在词尾，据说在词尾的也能成音节，会不会读得象汉语的“丝”一样就不得而知了。
τ　Τ　tau /tau,tay?/ 后面一部分得读音不得而知，/u/还是/y/？/t/不送气，所以应该类似“搭屋”/“搭淤”，而非“套”。
υ　Υ　ypsilon /y:psilo:n/ /y/类似汉语的“淤”而非“乌”，拉丁语里没有这个音，所以字母命名为 igraeca，即“希腊的i”的意思。与/i/部位相同，但是圆唇元音。
φ　Φ　phi [ fai ] /ph/表示送气音，所以应该类似“批”。
χ　Χ　chi /khi:/ c在古代拉丁语里的读音总是为/k/，/kh/为送气音。
ψ　Ψ　psi /psi:/
ω　Ω　omega /o:me:ga/ /o:/是长音，因为mega表示大的意思，即“大的o”

# JavaScript

- [ ] Udemy - The Complete JavaScript Course 2020: From Zero to Expert! 2020-10

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udmy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part5_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part6_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_The_Complete_JavaScript_Course_2020_From_Zero_to_Expert_2020-10.part7_Downloadly.ir.rar
  
- [ ] Udemy – JavaScript – The Complete Guide 2020 (Beginner + Advanced) 2020-10
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part1_Downloadly.ir.rar
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part2_Downloadly.ir.rar 
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part3_Downloadly.ir.rar
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part4_Downloadly.ir.rar
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part5_Downloadly.ir.rar
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part6_Downloadly.ir.rar
  http://dl3.downloadly.ir/Files/Elearning/Udemy_JavaScript_The_Complete_Guide_2020_Beginner_Advanced_2020-10.part7_Downloadly.ir.rar

# Python

- [ ] Udemy - Master Math by Coding in Python 2020-2

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part5_Downloadly.ir.rar


- [ ]  UDEMY – COMPLETE PYTHON DEVELOPER IN 2021: ZERO TO MASTERY 2020-10

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Complete_Python_Developer_in_2021_Zero_to_Mastery_2020-10.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Complete_Python_Developer_in_2021_Zero_to_Mastery_2020-10.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Complete_Python_Developer_in_2021_Zero_to_Mastery_2020-10.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Complete_Python_Developer_in_2021_Zero_to_Mastery_2020-10.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Complete_Python_Developer_in_2021_Zero_to_Mastery_2020-10.part5_Downloadly.ir.rar

- [ ] UDEMY – MASTER MATH BY CODING IN PYTHON 2020-2

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Master_Math_by_Coding_in_Python_2020-2.part5_Downloadly.ir.rar

# Data Base

- [ ] Udemy – Microsoft Access Complete Beginner to Advanced 2019-5

  http://dl.downloadly.ir/Files/Elearning/Udemy_Microsoft_Access_Complete_Beginner_to_Advanced_2019-5.part1_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_Microsoft_Access_Complete_Beginner_to_Advanced_2019-5.part2_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_Microsoft_Access_Complete_Beginner_to_Advanced_2019-5.part3_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_Microsoft_Access_Complete_Beginner_to_Advanced_2019-5.part4_Downloadly.ir.rar

# English

- [ ] UDEMY – IELTS VOCABULARY: LEARN 400 ESSENTIAL

  http://dl.downloadly.ir/Files/Elearning/Udemy_IELTS_Vocabulary_Learn_400_Essential_Words_for_IELTS_2019-10.part1_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_IELTS_Vocabulary_Learn_400_Essential_Words_for_IELTS_2019-10.part2_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_IELTS_Vocabulary_Learn_400_Essential_Words_for_IELTS_2019-10.part3_Downloadly.ir.rar

  http://dl.downloadly.ir/Files/Elearning/Udemy_IELTS_Vocabulary_Learn_400_Essential_Words_for_IELTS_2019-10.part4_Downloadly.ir.rar

- [ ] UDEMY – IELTS BAND 7+ COMPLETE PREP COURSE 2020-10

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part5_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part6_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_IELTS_Band_7_Complete_Prep_Course_2020-10.part7_Downloadly.ir.rar

# Excel

- [ ] Udemy - Microsoft Excel - Excel from Beginner to Advanced 2020-5 / 2020-7
  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part3_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part4_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part5_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Excel_from_Beginner_to_Advanced_2020-5.part6_Downloadly.ir.rar
# Formula
- [ ] Udemy - Microsoft Excel - Advanced Excel Formulas & Functions 2020-3

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Advanced_Excel_Formulas_Functions_2020-3.part1_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Advanced_Excel_Formulas_Functions_2020-3.part2_Downloadly.ir.rar

  http://dl3.downloadly.ir/Files/Elearning/Udemy_Microsoft_Excel_Advanced_Excel_Formulas_Functions_2020-3.part3_Downloadly.ir.rar

# Learning

## Subject

1. 控制论

## Book





# Backlog

## Level 1

1. 考研





## Level 2

1.接下来的五年计划