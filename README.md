# docker
## 安装
### 删除旧的docker
&ensp;&ensp;&ensp;&ensp;1.查询安装过的包    `yum list installed | grep docker` <br/> 
&ensp;&ensp;&ensp;&ensp;2.删除安装的软件包  `yum -y remove 【1中搜索到的docker】` <br/> 
&ensp;&ensp;&ensp;&ensp;3.删除镜像/容器等   `rm -rf /var/lib/docker` <br/> 

### 安装docker
#### 最新版本安装
##### 命令
&ensp;&ensp;&ensp;&ensp;`yum install docker-ce docker-ce-cli containerd.io` <br/>
#### 历史版本安装
&emsp;&emsp;查找历史版本：`yum list docker-ce --showduplicates | sort -r` <br/>

&emsp;&emsp;&emsp;&emsp;docker-ce.x86_64  3:18.09.1-3.el7                     docker-ce-stable <br/>
&emsp;&emsp;&emsp;&emsp;docker-ce.x86_64  3:18.09.0-3.el7                     docker-ce-stable <br/>
&emsp;&emsp;&emsp;&emsp;docker-ce.x86_64  18.06.1.ce-3.el7                    docker-ce-stable <br/>
&emsp;&emsp;&emsp;&emsp;docker-ce.x86_64  18.06.0.ce-3.el7                    docker-ce-stable <br/>

&emsp;&emsp;安装历史版本：`yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io`

#### 启动docker
&emsp;&emsp;`systemctl start docker`

#### 运行实例
&ensp;&ensp;&ensp;&ensp;&ensp;`docker run hello-world`

#### 发布image
&ensp;&ensp;&ensp;&ensp;&ensp;1.登录  `docker login`  <br/>
&ensp;&ensp;&ensp;&ensp;&ensp;2.重新构建image文件  `docker image build -t dosen2020/koa-demo:0.0.1 .`  <br/>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;【docker image build -t [username]/[repository]:[tag] .】 <br/>
&ensp;&ensp;&ensp;&ensp;&ensp;3.发布image文件 `docker image push dosen2020/koa-demo:0.0.1` <br/>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;【docker image push [username]/[repository]:[tag]】 <br/>
&ensp;&ensp;&ensp;&ensp;&ensp;4.登出 `docker logout`  <br/>

### 引用链接
&emsp;&emsp;<a href="http://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html" target="_blank">http://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html
