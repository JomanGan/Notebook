
# 

## 感受

### 从整体项目分工而言（手机项目）
- 安卓项目大致我把分为  bsp底层硬件端 framework框架端  App展示端
- 那么Repo也是凌驾于整个项目开发之上采用的
- 整个AOSP的源代码往往采取的就是用Repo来管理众多Git库，然后每个项目组负责针对个别的git仓的开展开发工作
- 具体的，整个repo大仓是由专门的部门负责维护，

### ‘底层’小组负责单个git
- 我们从base，一个到手的git，加上设计书上写满的各式各样且不断补充的一条条需求；我们开始了开发编码工作

### 开发阶段中的 大工 与 小工
- 理所应当，大工 管 小工 ， 精确些、项目leader（大工）review 组员（小工）的代码成果—— —— 一笔笔git的push提交
- 这个过程便是gerrit发挥的时候
- Gerrit：基于 Web 的代码评审和项目管理的工具；通俗讲就是Reveiw直观化工具


### 补充下命令流程
```bash
repo init xxx初始化
repo sync xxx同步要改动的项目
git commit本地提交改动
等别人通过gerrit review
review如果有需要改动的地方，那本地改好后，git commit --amend来保存新的修改
通过gerrit平台merge通过评审的代码
重复

```
### 关键点
1. 项目清单库(.repo/manifests)
2. 同时操作多个git库（repo forall -c "git add . ; git reset --hard xxxxx"）
