# docker
## 安装
### 删除旧的docker
&ensp;&ensp;&ensp;&ensp;1.查询安装过的包    yum list installed | grep docker <br/> 
&ensp;&ensp;&ensp;&ensp;2.删除安装的软件包  yum -y remove 【1中搜索到的docker】 <br/> 
&ensp;&ensp;&ensp;&ensp;3.删除镜像/容器等   rm -rf /var/lib/docker <br/> 

### 安装docker
#### 最新版本安装
##### 命令
&ensp;&ensp;&ensp;&ensp;yum install docker-ce docker-ce-cli containerd.io <br/>
#### 历史版本安装
&ensp;&ensp;&ensp;&ensp;查找历史版本：yum list docker-ce --showduplicates | sort -r <br/>
