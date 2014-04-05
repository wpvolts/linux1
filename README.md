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
*     

