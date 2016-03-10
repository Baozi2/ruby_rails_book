# Sass
```
@charset 'utf-8';
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
```
