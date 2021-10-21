配置

git config --global --list

等同文件

~/.gitconfig



//查

git config --global user.name

//增
git config  --global --add user.name jianan

//删
git config  --global --unset user.name

//改
git config --global user.name jianan


Git本地有四个工作区域：工作目录（Working Directory）、暂存区(Stage/Index)、资源库(Repository或Git Directory)、git仓库(Remote Directory)。文件在这四个区域之间的转换关系如下：

![img](https://img2018.cnblogs.com/blog/1090617/201810/1090617-20181008211557402-232838726.png)

workspace :代码存在的地方

index：暂存区 本质是个文件 作用保存即将提交的文件列表信息

repository：





workspace <---->index

```shell
$ git ls-files --stage
100644 ec1170b09aa0bcf2ac478ffef398ca352d54f18b 0       "git\345\221\275\344\273\244"

Cheney@LAPTOP-9VPBMD7H MINGW64 /d/code/gitlearn (master)
$ git add git.md

Cheney@LAPTOP-9VPBMD7H MINGW64 /d/code/gitlearn (master)
$ git ls-files --stage
100644 e69de29bb2d1d6434b8b29ae775ad8c2e48c5391 0       git.md
100644 ec1170b09aa0bcf2ac478ffef398ca352d54f18b 0       "git\345\221\275\344\273\244"

Cheney@LAPTOP-9VPBMD7H MINGW64 /d/code/gitlearn (master)
$ git reset git.md #撤销add到缓存区

Cheney@LAPTOP-9VPBMD7H MINGW64 /d/code/gitlearn (master)
$ git ls-files --stage
100644 ec1170b09aa0bcf2ac478ffef398ca352d54f18b 0       "git\345\221\275\344\273\244"
```



