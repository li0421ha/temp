# Github
## 关键字查询
	awesome,去此标签类别中查询项目
	python tutorial,查询资料，书籍，文档
	socket sample,查询对应技术的代码样本
## github 三要素
### Repository 仓库
	仓库是github项目管理存储基本单位
	一个仓库中存储一个项目，一个用户可以拥有多个仓库，一般仓库分为public,private
### Commit 提交
	程序员在整个开发周期，有大量的对代码的迭代和修改，都可以通过commit的方式进行记录，便于程序员回溯代码，即使这些代码被删除
	提交便于使用者观察整个工程的开发流程以及设计流程
### Branch 分支
	在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支位master / main
	不仅可以管理代码存储，便于多人协作开发
### 插入图片
[![1.png](https://i.postimg.cc/yWC8n3DV/1.png)](https://postimg.cc/FkGvHRbq)

### 仓库内容
	Code,资源存储，代码资源，二进制，项目管理脚本，许可证等等
	issues,使用时遇到的bug或进行提交，等待反馈
	README，使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等
	LICENSE许可证，GDL 2.0,3.0 Apahce 2.0, Mit,这些许可证，给使用者最大使用权限以及最少的限制
### Git软件，分布式版本控制系统
	仓库管理软件，使用git管理私人代码或者企业代码
[![2.png](https://i.postimg.cc/3J9XS2XS/2.png)](https://postimg.cc/56YQjYkL)
## 设备认证
### 1.如何让让网站的账户和设备绑定，后续完成代码的管理，上传下载
	git init  //创建本地仓库	*后续对仓库的操作，都要在仓库位置
[![3.png](https://i.postimg.cc/Y0D19HCc/3.png)](https://postimg.cc/30pySzG9)
	
	git config --list  //查看git的配置文件
[![4.png](https://i.postimg.cc/zDxwpnSd/4.png)](https://postimg.cc/Hj77k8N5)
	git config --global user.email"邮箱"
[![5.png](https://i.postimg.cc/wBkRMpwW/5.png)](https://postimg.cc/SXJx1wF8)
	git config --global user.name"用户名"
[![6.png](https://i.postimg.cc/1t5nNjTy/6.png)](https://postimg.cc/hJ6PkpcY)
	ssh-keygen -t rsa -C "注册邮箱"  //创建本地密文
	*去对应的目录查看密文文件，rsa.pub 复制密文，粘贴 settings -> SSH key and GPG -> new ssh key -> 粘贴
[![7.png](https://i.postimg.cc/rpgzc9p3/7.png)](https://postimg.cc/rd0qNxxN)
	ssh -T git@github.com  //测试关联是否成功
[![8.png](https://i.postimg.cc/jdXjyXH5/8.png)](https://postimg.cc/Whdjv0fL)
### 2.为目标仓库起别名，定位目标仓库，后续上传
	git remote add origin "ssh地址"  //为ssh仓库地址创建别名为origin
	git remote remove origin  //删除origin别名
## 本地设备与云端仓库的交互逻辑
[![9.png](https://i.postimg.cc/Y9qRq8zW/9.png)](https://postimg.cc/Y4ZYd6Vr)
## 代码更新的依赖关系被破坏
	本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致本地内容无法再次提交
	*先拉取git pull 云端内容 与本地内容合并或操作，而后再次推即可
	git pull --rebase origin master
	git rebase --skip "忽略本地内容 保留云端内容"
	git rebase --abort "忽略本地内容 保留云端内容"
	git rebase --continue "忽略本地内容 保留云端内容"
[![10.png](https://i.postimg.cc/RZ5TnvT9/10.png)](https://postimg.cc/LnDPcK70)
## 下载开源代码
	git clone "https仓库地址"  //下载开源项目code资源
## 分支Branch
	*关于分支的相关命令，创建分支、选择分支、合并分支等等
## Markdown,文本修饰语言，用特殊符号修饰正文效果<br>

## 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五级标题）


## 正文内容
   
   输入正文内容，但是如果需要换行，用\<br\>\ 标签

## 修饰正文

   *一段测试文本*

   **一段测试文本**

   ***一段测试文本***

   ~~一段测试文本~~

   这是一段测试文本，将`关键字`，重点显示
## 分割线
   
   用\-\-\- 表示分割线

---

## 引用效用\>表示
> 你自己就是一座金矿，关键在于如何挖掘和利用自己
>> 苏格拉底
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无序列表 \*
* 二次元
  * 原神
    * 神里凌华
* 大逃杀类
  * PUBG
  * APEX

### 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
   3. 凝聚态物理
2. 计算机科学
   1. 分布式架构
   2. 云计算
### 混合列表
1. 测试一级
   * 测试二级
   2. 测试三级

### 表格
名称|技能|排行
--|:--:|--:|
蝙蝠侠|有钱|32
海王|游泳|16
闪电侠|跑|18

### 代码片段

```c
	#include <stdio.h>
	int main(void)
	{
		printf("test code\n");
		return 0;
	}
```

```cpp
	#include <iostream>
```
```python
	import <os>
```
```bash
	echo "测试"
	pwd
	ps aux
	ls -l
```

### 超链接技术

[https://github.com/li0421ha/temp?tab=readme-ov-file](https://www.github.com "点击访问")

### 插入图片
![壁纸截图](C://Users//DELL//Desktop//是的我是神.jpg "悬停标题")

