###Github 简单使用
关键字查询  awesome,去此标签类别中查询项目
python tutorial,查询资料，书籍，文档
socket sample,查询对应技术的代码样本

###Github三要素
1. Repository仓库
仓库是github项目管理存储基本单位
一个仓库中存储一个项目，一个用户可以拥有多个仓库，一般仓库分为public,private

2. Commit提交
程序员在整个开发周期，有大量的对代码资源的迭代和修改，都可以通过commit的方式进行记录，便于程序员回溯代码，即使这些代码被删除
提交便于使用者观察整个工程的开发流程以及设计流程

3. Branch分支
在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支为master/main
不仅可以管理代码存储，便于多人协作开发
![协作图](C;//Users//lenovo//Desktop//1.jpg )

###仓库内容
1. Code,资源储存，代码资源，二进制，项目管理脚本，许可证等等
2. issues,使用时遇到的bug或进行提交，等待反馈
3. README,使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等<br>4. LICENSE许可证,以下这些许可证给使用者最大使用权限以及最少的限制
* GPL 2.0
 * GPL 3.0
  * Apahce 2.0
   * Mit

###Git软件，分布式版本控制系统
仓库管理软件，使用git管理私人代码或企业代码
![Git更新图](C;//Users//lenovo//Desktop//2.jpg )

###设备认证
1. 如何让网站的账户与设备绑定，后续完成代码的管理，上传下载
```bash
          git init //创建本地仓库
```
```bash
          git config --list  //查看git的配置文件
```
```bash
       	  git config --global user.email "邮箱"  //增加个人邮箱配置
```
```bash
	  git config --global user.name "用户名"  //增加个人名字配置
```
```bash
	  ssh-keygen -t rsa -C "注册邮箱"  //创建本地密文
```
去对应的目录查找密文文件

	rsa.pub 复制密文，粘贴  settings -> SSH key and GPG -> new ssh key ->粘贴
```bash
	ssh -T git@github.com  //测试是否关联成功
```

2. 为仓库起别名，定位目标仓库，后续上传
```bash
	git remote add origin "ssh地址"  //为ssh仓库地址创建别名为origin
```
```bash
	git remote remove origin  //删除origin别名
```
```bash
	git remote add origin "ssh地址"  //为ssh仓库地址创建别名为origin
```


![交互逻辑图](C;//Users//lenovo//Desktop//3.jpg )

```bash
	git add  //添加内容
```
```bash
	git rm  //删除本地文件并删除仓库数据
```
```bash
	git restore  //恢复被删除（仓库存在）
```

###代码更新的依赖关系被破坏

本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致本地内容无法再提交
解决办法：先拉取 git pull 云端内容 与本地内容合并或操作，而后再次推即可

```bash
	git pull --rebase origin master
```
```bash
	git rebase --skip  //忽略本地内容，保留云端内容
```
```bash
	git rebase --abort  //忽略本地内容，保留云端内容
```
```bash
	git rebase --continue  //忽略本地内容，保留云端内容
```

###下载开源代码
```bash
	git clone "https仓库地址"  //下载开源项目code资源
```


###分支Branch
关于分支的相关命令，创建分支，选择分支，合并分支等等


Markdown ,github可以编写readme，文本修饰语言，用特殊符号修饰正文效果<br>

#标题修饰符（一级标题）\#
##（二级标题）
###（三级标题）
####（四级标题）
#####（五级标题）

##正文内容

输入正文内容，但是如果需要换行，用\<br\>标签

##修饰正文

*一段测试文本*
**一段测试文本**
***一段测试文本***
~~一段测试文本~~

## 分割线

用\-\-\- 表示分割线

##引用效用\>表示
> 顾雪纯
>> yuki
>>> yoky
>>>> 雪山樱花

## 列表修饰符
### 无序列表 \*
* 小说
 * 纯爱
  * 爱看
* 游戏
 * 吃鸡
 * 王者荣耀

###有序列表
1. 物理学
   1. 原子物理
   2. 核物理
   3. 凝聚态物理
2. 计算机科学
   1. 软件工程
   2. 大数据

### 混合列表
1. 测试一级
* 小说
 * 爱看
2. 测试二级
 1. 油壶

### 表格
名称|技能|排行
--|:--:|--:
蝙蝠侠|有钱|32
海王|钓鱼|1
闪电侠|跑|108

### 代码片段

```c
          #include<stdio.h>
	  int main(){
	  printf("hello world\n");
	  return 0;
	  }
```
```cpp
           #include<iostream>
```
```python
           import <os>
```
```bash
          echo"测试"
	  pwd
	  ps aux
	  ls -l
```

### 超链接技术
[Github](https://www.github.com "点击访问")

### 插入图片 只是记载格式，此图片并未真实存在
![壁纸截图](C;//Users//cui88//Desktop//1.jpg )


