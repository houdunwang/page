#分页

分页组件可以产生基于当前页面的智能「范围」链接，所产生的 HTML 兼容 Bootstrap CSS 框架.

[TOC]

####创建实例

```
$obj = new \houdunwang\page\Page();
```

####根据数量获取分页

```
echo $obj->make(100);
```

####显示分页

```
echo $obj->show();
```

####获取所有分页属性

可以获取分页属性，如 文字页码、图形页码、下拉列表页码等

```
$obj->all(100);
```
####设置每页显示条数

```
$obj->row(8)->make(100);
```

####设置页码数量

```
$obj->pageNum(5)->make(100);
```

####自定义url

```
echo $obj->url('list/{page}.html')->make(100,1);
```

####定义显示文字

```
echo $obj->desc(['pre'=>'上楼', 'next'=>'下楼','first'=>'首页','end'=>'尾页','unit'=>'个'])->make(200,2);
```

####返回limit语句

```
$obj->limit();
```

####取得所有形式用于定义

```
$info= $obj->all(200);
print_r($info);
```

####获取分页的总页数

```
$obj->totalPage();
```