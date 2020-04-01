# 流媒体中的CDN与P2P
## P2P组播
### 挑战
- 实时性，需要一定程度上保证数据顺序到达
- 带宽
- 用户期望
- 高churn rate（用户的动态性）
- 公平性，有人不愿上传
### 解决
#### 树形结构
问题：如何维护，上层节点推出影响大，底层节点带宽利用率不高

![1584423781567](CDN%E4%B8%8EP2P.assets/1584423781567.png)

### Mesh结构

类似Swarm

#### Step 1 

和一些周围节点建立连接

#### Step2 block scheduling

交换相互的数据块

![1584424546964](CDN%E4%B8%8EP2P.assets/1584424546964.png)

400k带宽-上万人播放

在线用户越多，系统性能越好

#### 挑战

Incentive fairness

设备异构性

客户端代码

部署

#### 商用

无法收费，因为无法保证

## CDN

Origin Server - edge server - customer

### 部署

位置、访问

判断流行度

![1584425592724](CDN%E4%B8%8EP2P.assets/1584425592724.png)

#### 案例Netflix

基于aws，三家CDN，有rank

视频分段 4s左右，不断请求

对每个用户，静态CDN排序

太差则更换

