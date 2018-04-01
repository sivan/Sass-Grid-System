# Sass Grid System

## 简单介绍

一个方便 Sass 使用的网格系统，来自 Blueprint。

* `$column-width`: 栏宽度;
* `$gutter-width`: 槽宽度;
* `$columns`: 网格数量;

## 使用方式

在响应 ID 或 class 中使用

``` sass
@include grid(column, col-type);
```

* 第一个参数 column 为网格数，设定为 `wrap` 时为网格容器。
* 第二个参数 col-type 为网格类型，默认可以留空，每行末尾元素使用 `last`。也可以使用 `append`、`prepent`、`pull`、`push` 来实现不同布局。

如实现下面的网格布局，原来的 CSS 代码为：

``` sass
.container {
  width: 988px;
  margin: 0 auto;
}
.content-main {
  width: 652px;
  float: left;
  margin-right: 20px;
}
.content-sub {
  width: 316px;
  float: left;
  margin-right: 0;
}
```

在载入本框架后，代码如下

``` sass
  .container {
    @include grid('wrap');
  }
  .content-main {
    @include grid(12);
  }
  .content-sub {
    @include grid(6, 'last');
  }
```

## 更多说明

本代码适合布局简单的页面使用，去掉网格系统中纯粹的布局标记，大幅精简 **HTML** 中的冗余代码，如 `span-13`、`column`、`append-6` 等。

但当页面布局、层级复杂时，还是使用传统方式更佳。

-- EOF --
