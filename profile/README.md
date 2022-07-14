# 项目git规范

## 分支管理

### 分支建立

**默认分支**

master为稳定主分支，适用于稳定版本代码管理

dev为开发默认主分支，适用于开发迭代，最终合并所有新功能、BUG修复、优化处理

**新功能或优化分支**

新功能或优化分支，功能点为基础，以feature-开头建立分支

如图片视频选择器，则以feature-media-picker建立分支

**修复BUG分支**

修复BUG分支，BUG点为基础，以fix-开头

如修复数据库保存错误，则以fix-db-write-error建立分支

### 分支合并

新功能/优化/修复BUG分支合并至dev(开发默认分支)，确保合并前基础分支为最新基线。

> feature-new-item 合并至dev分支，feature-new-item是由几天前dev分支的版本建立，则feature-new-item 基线并非为dev分支的最新基线。需要通过git rebase将feature-new-item基线更新到最新，再合并到dev

