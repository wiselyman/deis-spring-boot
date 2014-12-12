deis-spring-boot
================

部署spring boot jar程序到deis的模板

**这个模板允许:**
- 使用一个spring boot 的fat jar
- 修改默认的JVM设置
- 使用 [Procfile](https://devcenter.heroku.com/articles/procfile)

**步骤:**
- 下载,可选择下载zip，或者`git clone`
- 编辑launch.sh,使用正确的jar地址替代JAR_FILE=?
- 将jar包放在当前目录

**使用buildpacks部署spring boot jar 详细步骤:**
- 生成一个ssh key，可使用安装deis的ssh key
- 在注册好deis用户后，执行` deis keys:add `按照提示操作
- 执行eval `ssh-agent -s`  
- 执行`ssh-add ~/.ssh/deis`
- `git clone https://github.com/wiselyman/deis-spring-boot.git`
- `cd deis-spring-boot`
- `deis create app_name`
- `git push deis master`
