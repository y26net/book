## ubuntu 安装 docker 并配置镜像加速(使用 apt-get 进行安装)

```
# 1. 卸载docker
sudo apt-get remove docker docker-engine docker.io containerd runc

# 2. 更新包索引
sudo apt-get update

# 3. 安装依赖
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

# 4. 添加 docker 官方 GPG 密钥
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# 5. 添加安装 docker 软件源
# 这个是官方的
# sudo add-apt-repository \
#    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
#    $(lsb_release -cs) \
#    stable"
# 使用阿里云的源比较快
sudo add-apt-repository "deb [arch=amd64] https://mirrors.aliyun.com/docker-ce/linux/ubuntu $(lsb_release -cs) stable"

# 6. 更新软件包索引
sudo apt-get update

# 7. 安装docker相关的	docker-ce 社区版	ee企业版
sudo apt-get -y install docker-ce docker-ce-cli containerd.io

# 8. 跑一下
sudo docker run hello-world

# 如果报错了就启动一下 docker 服务再去跑
sudo service docker start
```