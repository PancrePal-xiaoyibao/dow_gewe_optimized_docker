
# 本项目是基于DOW和GEWE官方的社区定制版，感谢DOW作者和GEWE团队的贡献！每一位患者/家属的使用，都离不开他们的风险！

# 增强功能
1. 图像识别：提供对于病情报告的识别，解读，患者再也不用求人，自己就可以随时掌握报告指标的定义和含义。这里特别感谢阶跃星辰提供了优秀和领先的多模态模型step-1o-vision，强烈推荐！！

2. 插件能力：
2.1 临床试验查询
2.2 药品查询
2.3 AI智能搜索（metaso）
2.4.营养视频（感谢复旦肿瘤医院胰腺综合治疗部的内容开源和授权）
2.4 生活便利
* 天气查询：方便出行
* 音乐点播：改善心情
* 菜谱制作
* 美团外卖

---
# 镜像地址

```json
docker login ccr.ccs.tencentyun.com --username=100015489703

密码 咨询田老师/飞书权限

docker pull ccr.ccs.tencentyun.com/xiaoyibao/dow-gewe-official-simplified-xyb:v5
```
---
# 配置说明：
## docker-compose.yml配置中，端口映射配置需要和公网开放的端口一致。家里我直接偷懒，用了9919端口，转发到本地MAC电脑IP的9919端口。    
```json
        ports:
      - "9919:9919"
```


# config.json配置中，必须是公网IP + 公网开放的端口才可以。
```json
    "gewechat_callback_url": "http://112.65.86.214:9919/v2/api/callback/collect"
```

重启后就可以启动了，扫码登录。

# 修改插件
```json
- plugins/hello中修改欢迎词
- plugins/lcard中修改和增加卡片
- 插件过多容易封号


----
# 后续开发计划
[]更多病友需要的插件能力
[]Medgemma3的接入
[]企业微信的支持版本（其它志愿者的贡献)
...

# 关于社区
#小胰宝 是一个病友自助开始的项目，23年创立，24年中开源发展，24年底捐献给天工开物基金会，25年升级为社区化，由基金会和社区管理委员会CMC管理，构建纯血版的AI类公益开源项目- #小X宝社区，积极推动跨社区合作，专业推动社区规范管理，目前生态人群180+。社区目的是推动AI技术和RAG应用的普及化，集合力量助力25+癌种患者，并延伸至280+罕见病领域，立足患者公益服务，通过技术+任务，有效减少医患信息差，推动患者/家属规范治疗，减低焦虑。目前已经推出了小胰宝助手，小肺宝助手，小萌宝助手，小粉宝助手，小胃宝，小妍宝，小飞侠助手（首个罕见病领域应用）等项目。

## 了解社区

社区具备公益x开源双重属性,属于AI社区中的创新社区
👀 了解社区, 可以点击 [社区介绍](https://hi.xiao-x-bao.com.cn)
‼️ 了解更多志愿者的责任，点击 [志愿者FAQ](https://faq.xiao-x-bao.com.cn)
❤️ 考虑好了，click "i am in", 点击加入我们 [加入页面](https://iamin.xiao-x-bao.com.cn)
😊 社区任务全透明化，不仅开放阅读，也开放了创建，鼓励志愿者加入自己的梦想项目 [任务中心](https://task.xiaoyibao.com.cn)
👌 首个贡献：您的辅导员，会和您一起沟通介绍，帮助您在第一周确定首个贡献计划 [First Good Issue](https://myfirst.xiao-x-bao.com.cn)
欢迎体验demo: 
⭐️ 小胰宝3个版本：[科普版](https://chat.xiaoyibao.com.cn)、[Pro版](https://pro.xiaoyibao.com.cn)、[Deepseek版](https://deepseek.xiaoyibao.com.cn)
⭐️ 小肺宝: [小肺宝](https://chat.xiaofeibao.com.cn)
⭐️ 小萌宝: [小萌宝](https://pro.xiaomengbao.cn/)
⭐️ 小粉宝：[小粉宝](https://xfb.xiaoyibao.com.cn) (后续会有独立域名)
⭐️ 小胃宝: [科普版](https://chat.xiaoweibao.com.cn)、[专业版](https://pro.xiaoweibao.com.cn) (首个社区合作项目)

欢迎加入社区贡献项目：
👏 [小X宝社区"AI探宝计划"](https://wiki.xiao-x-bao.com.cn) - 为推广患者个人掌握智能体构建
👏 标准的github/gitcode上的代码和项目贡献 我们已经开源了3个项目仓库，包括：
  - [小胰宝](https://github.com/PancrePal-xiaoyibao/miniapp-uniapp)
  - [MinerU-xyb](https://github.com/PancrePal-xiaoyibao/miniapp-uniapp)
  - [fastgpt-on-wechat](https://github.com/hanfangyuan4396/fastgpt-on-wechat)
  - [Gemini-2.0病情demo](https://github.com/PancrePal-xiaoyibao/gemini2.0-xiaoyibao)
期待更多开源加入完善社区，提供开源能力；
👏 [小X宝社区"胰腺肿瘤并发症病友共创宝典"](https://bfz.xiao-x-bao.com.cn) - 开放病友共创的第一个标准wiki