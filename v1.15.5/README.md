1、安装docker版本19.03.8(官网下载或者通过下面的链接)

    链接:https://pan.baidu.com/s/1U1F05APvBXAI4nL1oMVBUQ  密码:lj4v  【MAC】
    
    链接:https://pan.baidu.com/s/1GBCG0_1A1bTtxmU1lyaTkA  密码：7v45 【WIN-Docker-2.2.0.5】

2、配置资源：

    3CPU/6G（自己按需设置）
    
3、添加镜像：

    我是用的是阿里云镜像地址

4、下载镜像：

    执行脚本：sh ./images.sh

    查看镜像：docker images

5、设置打开

    5.1、启动Kubernetes:Docker-->Preference-->Enable Kubernetes

    注：等待kubernetes启动完成、如果长时间未启动通过查看启动日志或者查看依赖镜像是否下载完整

   
    5.2、启动完成执行如下操作：
   
    kubectl config use-context docker-desktop
   
    kubectl cluster-info
   
    kubectl get nodes
   
    kubectl apply -f kubernetes-dashboard.yaml
   
    
    5.3、开启代理访问：kubectl proxy
  
    
    5.4、页面访问地址：http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy

6、获取令牌: 

    sh ./access.sh
    
7、详情参考：

    https://my.oschina.net/wubiaowpBlogShare/blog/4261466
    
