```
@charset 'utf-8';

@import 'base';//引入的scss文件会自动合并成一个 被引入的scss文件 一般以_开头 忽略扩展名
@import 'base1.css';
/*windows下编码问题
*Encoding.default_external = Encoding.find('utf-8')
*/
// 单行注释 不会编译到css文件中
/*
* 多行注释会编译到css文件中
*/
//sass xxx.scss  xxx.css  将xxx.scss 编译成 xxx.css文件
//sass --wathc  xxx.scss:xxx.css  实时编译
$fontSize: 12px;//定义变量
$fontColor: #f00;
body{
    font-size: $fontSize;
    font-color: $fontColor;
}
// 如果变量作为属性值或者特殊情况下 必须以#{variables}形式使用
//应用于class和属性
$borderDirection:       bottom;//覆盖默认值
$borderDirection:       top !default;//!default 设置默认变量

.border-#{$borderDirection}{
	border-#{$borderDirection}: 1px solid #f00;
}
//用于复杂属性
$baseFontSize:          12px !default;
$baseLineHeight:        1.5 !default;
body{
	font: #{$baseFontSize}/#{$baseLineHeight};
}
```