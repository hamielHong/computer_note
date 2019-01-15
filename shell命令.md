shell命令
===

1. setx **设置环境变量**

    设置用户环境变量 -- `setx ENV_NAME env_value`

    设置系统环境变量 -- `setx ENV_NAME env_value /m`

    示例：`setx Path "%Path%;newpath1;newpath2" /m`

2. cd **切换目录**

    `/d` -- 支持切换磁盘分区

    `cd /d %~dp0` -- 更改当前目录为批处理本身的目录

    - %0代表批处理本身 d:\qq\a.bat
    - ~dp是变量扩充
    - d既是扩充到分区号 d:
    - p就是扩充到路径 \qq
    - dp就是扩充到分区号路径 d:\qq

3. copy **复制**

    `/y` -- 文件名重复不提示直接覆盖

    示例：`copy /y a.bat C:\`

4. echo **显示此命令后的字符**

5. echo off **在此语句后所有运行的命令都不显示命令行本身**

6. @ **与echo off相象，但它是加在每个命令行的最前面，表示运行时不显示这一行的命令行（只能影响当前行）**

7. call **调用**

    可以调用别的bat，也可以调用本bat内的标签

    标签：`:label`

8. set **设置各种shell选项或者显示系统中已经存在的shell变量，以及设置shell变量的新变量值**

9. if a==b () else ()