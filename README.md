linux基本命令使用
======
文件和目录
------
###目录跳转、查看###
*    cd /home 进入 '/ home' 目录'     //Tab可以自动补全
*    cd .. 返回上一级目录
*    cd ../.. 返回上两级目录 
*    cd 进入个人的主目录 
*    cd - 返回上次所在的目录 
*    pwd 显示工作路径 
*    ls 查看目录中的文件 
*    ls -F 查看目录中的文件 
*    ls -l 显示文件和目录的详细资料 
*    ls -a 显示隐藏文件 


###复制、删除、新建等文件夹操作###
*    mkdir dir1 创建一个叫做 'dir1' 的目录' 
*    mkdir dir1 dir2 同时创建两个目录 
*    mkdir -p /tmp/dir1/dir2 创建一个目录树 
*    rm -f file1 删除一个叫做 'file1' 的文件' 
*    rmdir dir1 删除一个叫做 'dir1' 的目录' 
*    rm -rf dir1 删除一个叫做 'dir1' 的目录并同时删除其内容 
*    rm -rf dir1 dir2 同时删除两个目录及它们的内容 
*    mv dir1 new_dir 重命名/移动 一个目录 
*    cp file1 file2 复制一个文件 
*    cp dir/* . 复制一个目录下的所有文件到当前工作目录 
*    cp -a /tmp/dir1 . 复制一个目录到当前工作目录 
*    cp -a dir1 dir2 复制一个目录 


软件安装
------
*    install + 软件名 （Tab查找补全）


编程
------
*    vim d.c     //进入文件编辑 i：进入编辑状态; Esc:退出编辑，再Shift+：wqb:保存退出
*    gcc -E d.c -o d.i
*    gcc -S d.i -o d.s
*    gcc -c d.i -o d.o
*    gcc d.o -o d
*    ./d          //  可以运行了


计算器使用
------

###通常我们使用是bc：###

    [tiger@liufofu ~]$ bc         //输入bc
    bc 1.06
    Copyright 1991-1994, 1997, 1998, 2000 Free Software Foundation, Inc.
    This is free software with ABSOLUTELY NO WARRANTY.
    For details type `warranty’.
    1+1
    2
    要求保留小数点的做法是：
    scale=2;1/2
    0.50

###bc结合管道的用法：###
        
    [tiger@liufofu ~]$ echo 1+1 | bc
    2

###bc结合ibase和obase的用法：###

    ibase是输入数字的进制，而obase就是输出数字的进制了。很好记，i是input，o是output
    [tiger@liufofu ~]$ echo “obase=16;17″ | bc
    11
    [tiger@liufofu ~]$ echo “ibase=16;17″ | bc
    23

###10进制与2进制的转换：###

    [tiger@liufofu ~]$ echo “ibase=10;obase=2;10″ | bc
    1010

###bc计算文件里的数值：###

    [tiger@liufofu ~]$ cat test.bc
    1+2
    [tiger@liufofu ~]$ bc test.bc
    bc 1.06
    Copyright 1991-1994, 1997, 1998, 2000 Free Software Foundation, Inc.
    This is free software with ABSOLUTELY NO WARRANTY.
    For details type `warranty’.
    3

echo 批量处理
------

###创建一个txt并且把字符串输入进去###

    echo “hello word” >input/f2.txt
