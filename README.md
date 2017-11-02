# MulticsDevOps
## 服务部署笔记 & 学习笔记 & 源代码-使用教程。
### Docker&kubernetes
* [给Docker配置官方国内加速镜像](https://github.com/MulticsYin/MulticsDevOps/blob/master/Docker/%E7%BB%99Docker%E9%85%8D%E7%BD%AE%E5%AE%98%E6%96%B9%E5%9B%BD%E5%86%85%E5%8A%A0%E9%80%9F%E9%95%9C%E5%83%8F.md)  
出于网路原因，国内访问 Docker Hub 有时会遇到困难，下载官方镜像更是望穿秋水。该教程解决这个问题，配置国内镜像加速器，为镜像下载加速。

### Git&GitHub
* [Ubuntu16.04下Git&Gitosis服务器安装与配置](https://github.com/MulticsYin/MulticsDevOps/blob/master/Git-Github/Ubuntu16.04%E4%B8%8BGit&Gitosis%E6%9C%8D%E5%8A%A1%E5%99%A8%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE.md)  
在实验室或者公司内部搭建一个局域网Git服务器(使用git和gitosis)。

### Web 相关
* [如何免费的让网站启用HTTPS](https://github.com/MulticsYin/MulticsDevOps/blob/master/Web/free_HTTPS.md)[转]  
使用 `Let’s Encrypt` 免费的解决方案。`Let’s Encrypt` 是一个于2015年推出的数字证书认证机构，将通过旨在消除当前手动创建和安装证书的复杂过程的自动化流程，为安全网站提供免费的SSL/TLS证书。  

* [负载均衡层技术](http://blog.csdn.net/column/details/load-balancing.html)（CSDN博客链接）  
主流负载均衡技术在HTTP系统中的应用，详细介绍了负载均衡系统涉及的主要设计思想，重点讲解了Nginx、LVS、Keepalived技术原理和使用方式。

* [负载均衡层技术(补充) - HAProxy](https://github.com/MulticsYin/MulticsDevOps/blob/master/Web/LoadBalancing.md)  
HAProxy是基于TCP四层和HTTP七层的开源的第三方应用负载均衡软件。具有高可靠性、高稳定性、高并发处理能力、透明代理和支持ACL功能等特点。HAProxy是一个功能强大且优秀的负载均衡集群解决方案。

* [Web系统的架构分层](https://github.com/MulticsYin/MulticsDevOps/blob/master/Web/WebSystem.md)

### 分布式系统相关组件
* [ZooKeeper](https://github.com/MulticsYin/MulticsDevOps/blob/master/DistributedSystems/Zookeeper.md)  
ZooKeeper是源代码开放的分布式协调服务，由雅虎创建，是Google的开源实现。ZooKeeper是一个高性能的分布式数据一致性解决方案，他将那些复杂的、容易出错的分布式一致性服务封装起来，构成一个高效可靠的原语集，并提供一系列简单易用的接口给用户使用。  

* [Kafka中文教程](http://www.orchome.com/kafka/index)（OrcHome链接）  
Kafka是由LinkedIn开发的一个分布式的消息系统，使用Scala编写，它以可水平扩展和高吞吐率而被广泛使用。  

### 微服务 - Micro service
* [认证鉴权与API权限控制在微服务架构中的设计与实现](http://blueskykong.com/categories/Security/)(转载)  
系统微服务化后，原有的单体应用是基于Session的安全权限方式，不能满足现有的微服务架构的认证与鉴权需求。微服务架构下，一个应用会被拆分成若干个微应用，每个微应用都需要对访问进行鉴权，每个微应用都需要明确当前访问用户以及其权限。尤其当访问来源不只是浏览器，还包括其他服务的调用时，单体应用架构下的鉴权方式就不是特别合适了。在微服务架构下，要考虑外部应用接入的场景、用户–服务的鉴权、服务–服务的鉴权等多种鉴权场景。  
比如用户A访问User Service，A如果未登录，则首先需要登录，请求获取授权token。获取token之后，A将携带着token去请求访问某个文件，这样就需要对A的身份进行校验，并且A可以访问该文件。  
为了适应架构的变化、需求的变化，auth权限模块被单独出来作为一个基础的微服务系统，为其他业务service提供服务。
