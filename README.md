# git-hook-node-demo

本项目展示了通过 git hook 来校验代码仓库提交信息的规范。  
实现方式为在做`git commit`操作时，会检查`commit message`的内容，如果不符合格式，会阻断提交过程。 

操作步骤：
1. 在需要应用的项目中执行 `npm install husky -D`，安装 husky 依赖，此依赖主要用于解决githook的内容无法纳入版本管理工具的问题。
2. 执行 `npx husky install`，初始化`.husky`目录。
3. 将本项目中 `prepare-commit-msg` 文件拷贝至`.husky`目录下。
4. 在触发提交操作后，规范门禁会起作用。

注：相关规则配置在`.husky/prepare-commit-msg`中，如果需要调整规则，请修改这个文件。
