#Sass Grid System

##简单介绍
一个方便 Sass 使用的网格系统，来自 Blueprint。还有待完善。

* $column-width: 栏宽度;
* $gutter-width: 槽宽度;
* $columns: 网格数量;

##使用方式
在响应 ID 或 class 中使用 

	@include grid(column, col-type);
	
* column 为栅栏数
* col-type 为栅栏类型，默认可以留空，每行末尾元素使用 `last` 即可。
* col-type 还可以使用 `append`、`prepent`、`pull`、`push` 来实现不同布局。

##更多说明
使用本系统可以大幅精简 **HTML** 中的冗余代码（如“`span-13`”、“`column`”、“`append-6`”等），适合布局简单的页面使用，去掉网格系统中纯粹的布局标记。

但注意当页面布局、页面层级复杂时，还是使用传统方式更佳。