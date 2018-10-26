



# 准备工作
    pip install --upgrade boto3
    pip install --upgrade boto3
    pip install awscli
    aws configure


# 身份验证
    #参考 https://docs.aws.amazon.com/zh_cn/AmazonECR/latest/userguide/Registries.html#registry_auth
    aws ecr get-login --no-include-email
    docker login -u AWS -p token== https://xxxx.dkr.ecr.cn-north-1.amazonaws.com.cn

# 获取仓库
    aws ecr describe-repositories

# 获取指定仓库镜像列表
    aws ecr describe-images --repository-name repo_name

# 拉取镜像
    docker pull xxxx.dkr.ecr.cn-north-1.amazonaws.com.cn/repo_name:image-tag-name

# 重命名镜像
    docker tag src_repo:src_tag obj_repo:obj_tag

# 删除旧镜像
    docker rmi old_repo:old_tag



~~完~~

