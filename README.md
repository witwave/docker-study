### docker 学习备忘录
以下所有操作环镜为`ubuntu 14.04LTS Docker version 1.6.2, build 7c8fca2`  
-查找镜像
`docker search ubuntu `

-获取镜像
`docker pull ubuntu`

-运行ubuntu这个镜像，进行交互模式
`docker run -it ubuntu /bin/bash`

-查看正在运行的容器
`docker ps`

-查看容器日志
`docker logs -f desperate_swartz`

-将工作目录挂载到容器中
`docker run -it  -p 8090:8090 -v /home/witwave/project/web:/opt/wtt  ubuntu`

-导出容器
`docker export -o ubuntu-node.tar 1823fe0dbcd9`

-导入本地镜像
`cat ubuntu-node.tar | docker import witwave:node`

-运行测试导出的本地镜像
`docker run -it  -p 8090:8090 -v /home/witwave/project/web:/opt/wtt/web  witwave:node /bin/bash`

-删除容器
`docker rm xxxxx-container`

-删除镜像
`docker rmi xxx-image`




