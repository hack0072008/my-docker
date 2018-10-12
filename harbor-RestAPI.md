

# 参考：
    https://www.cnblogs.com/guigujun/p/8352983.html

## 获取项目信息
    curl -u "admin:Harbor12345" -X GET -H "Content-Type: application/json" "http://10.100.102.207/api/projects?project_name=camera"

## 删除项目
    curl  -u "admin:Harbor12345"  -X DELETE  -H "Content-Type: application/json" "https://192.168.56.106/api/projects/{project_id}"

## 创建项目
    curl -u "admin:Harbor12345" -X POST -H "Content-Type: application/json" "https://192.168.56.106/api/projects" -d @createproject.json

## 删除项目成员
    curl -u "admin:Harbor12345" -X DELETE -H "Content-Type: application/json" "https://192.168.56.106/api/projects/{project_id}/members/{user_id}"


## 查询用户
    curl -u "admin:Harbor12345" -X GET -H "Content-Type: application/json" "http://10.100.102.207/api/users"

## 注册用户
    curl -u "admin:Harbor12345" -X POST -H "Content-Type: application/json" "https://192.168.56.106/api/users" -d @user.json

## 删除用户
    curl -u "admin:Harbor12345" -X DELETE  -H "Content-Type: application/json" "https://192.168.56.106/api/users/{user_id}"

## 修改用户密码
    curl -u "admin:Harbor12345" -X PUT -H "Content-Type: application/json" "https://192.168.56.106/api/users/{user_id}/password" -d @uppwd.json

## 获取镜像
    curl -u "admin:Harbor12345" -X GET -H "Content-Type: application/json" "https://192.168.56.106/api/repositories?project_id={project_id}&q=dcos%2Fcentos"

## 删除镜像
    curl -u "admin:Harbor12345" -X DELETE -H "Content-Type: application/json" "https://192.168.56.106/api/repositories?repo_name=dcos%2Fetcd "

## 搜索镜像
    curl  -u "admin:Harbor12345"  -X GET -H "Content-Type: application/json" "https://192.168.56.106/api/search?q=nginx"

## 获取镜像tag
    curl -u "admin:Harbor12345" -X GET -H "Content-Type: application/json" "https://192.168.56.106/api/repositories/tags?repo_name=dcos%2Fcentos"





