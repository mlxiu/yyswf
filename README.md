# yy魔法礼物，yy坐骑，yy动画，yyswf

`github` 上本来是禁止上传 `swf` 文件的。其判断也仅仅是文件后缀，而不是你文件实质。这里，通过shell将swf批量重命名，后边加上了 "_xxx_"。所以，使用的时候，需要去掉其后边追加的字符。


# shell 批量在文件名尾部添加 _xxx_ 字符

```
cd one

for i in `ls`;

do mv -f $i `echo $i"_xxx_"`;

done
```

# shell 批量去掉文件名后边的 _xxx_ 字符

```
cd one

for i in `ls`;

# 将后边的8位字符改成swf
do mv -f $i `echo $i | sed 's/........$/swf/'`;

done
```
