# 编译原理

## 第一章 引论

### 翻译程序

![翻译程序](image/compilation/翻译程序定义.png)

### 编译程序

![编译程序](image/compilation/编译程序.png)

**分类**:

![编译程序分类](image/compilation/编译程序分类.png)

### 解释程序

![解释程序](image/compilation/解释程序.png)

### 编译过程

![编译过程](image/compilation/编译过程.png)

**词法分析**:

![词法分析](image/compilation/词法分析.png)

**语法分析**:

![语法分析](image/compilation/语法分析.png)

**中间代码产生**:

![中间代码产生](image/compilation/中间代码产生.png)

**优化**:

![优化](image/compilation/优化.png)

**目标代码生成**:

![目标代码生成](image/compilation/目标代码产生.png)

### 编译程序逻辑结构

![编译程序逻辑结构](image/compilation/编译程序逻辑结构.png)

### 表格与表格管理

![表格与表格管理](image/compilation/表格.png)

### 出错处理

![出错处理](image/compilation/出错处理.png)

### 遍（Pass)

![遍（Pass)](image/compilation/遍.png)

### 编译前端和后端

![编译前端和后端](image/compilation/编译前端与后端.png)

### 参数传递

![参数传递](image/compilation/参数传递.png)

### 存储管理

![存储管理](image/compilation/存储管理.png)

## 第二章 高级语言及其语法描述

### 程序语言定义

![程序语言定义](image/compilation/程序语言定义.png)
> 文法：描述语言的语法结构的形式规则（即语法规则）。
>
> 上下文无关文法组成：一组终结符、一组非终结符、一个开始符号、一组产生式。

### 文法形式化定义和分类

**形式化定义**：
![文法形式化定义](image/compilation/文法形式化定义.png)

**分类**：
![分类](image/compilation/文法分类.png)
> 左线性文法：A->Ba或A->a，和右线性类似。
>
> 正规文法只能出现单个终结符，右线性文法中可能出现若干个终结符组成的串。
>
> 2型文法补充：A->ε。

四个文法类的定义是逐渐增加限制的，因此每一种正规文法都是上下文无关的，每一种上下文无关文法都是上下文有关的，而每一种上下文有关文法都是0型文法。

称0型文法产生的语言为0型语言。上下文有关文法、上下文无关文法和正规文法产生的语言分别称为上下文有关语言、上下文无关语言和正规语言。

现今大多数高级程序设计语言采用上下文无关文法来描述其语法已经足够了。

### 文法和语言

**推导和归约**：
![定义1](image/compilation/推导与归约1.png)
![定义2](image/compilation/推导与归约2.png)
![定义3](image/compilation/推导与归约3.png)

**最左推导和最右推导**：
![定义](image/compilation/最左推导与最右推导.png)
> 最右直接推导又称为规范直接推导，最右推导称为规范推导

**最左归约和最右归约**：
![定义](image/compilation/最左归约和最右归约.png)
> 最左推导的逆过程是最右归约，最右推导的逆过程是最左归约

**句型、句子、语言**：
![定义](image/compilation/句型句子语言.png)

**文法等价**：如果两个文法定义的语言一样，则称这两个文法等价。

### 语法分析树

**语法分析树**：
![语法分析树](image/compilation/语法分析树.png)

**文法二义性**：
![定义](image/compilation/文法二义性.png)
