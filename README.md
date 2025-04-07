# PPTX 生成服务

## 概述
本项目提供AI生成PPT服务，采用xai → .text.md → .pptx的转换流程。系统对符合Marp标准的.md文件有良好的转换效果。

## 快速开始

### 1. 获取镜像

docker pull crpi-1coe6qanb02szvo8.cn-beijing.personal.cr.aliyuncs.com/xiaojiangtm/aippt_create:1.0.1

### 2. 运行容器

docker run -d -v < your path >:/tmp/pptx -e TEMP_DIR=/tmp/pptx -p < your port >:5000

### 3. 调用API

请求地址：
http://< Your IP or Domain >:< port >/generate-pptx

请求头：
{
  "Content-Type": "application/json"
}

请求体：
{
  "content": "<your .md ppt>"
}

## 示例请求
{
  "content": "# 快速烹饪指南 - 鱼香肉丝\n\n## 美味家常菜 - 一步步教你做出地道川味\n\n制作者：[你的名字]  \n日期：[填写日期]\n\n---\n\n## 目录\n1. 菜品简介\n2. 材料清单\n3. 前期准备\n4. 烹饪步骤\n5. 小技巧\n6. 总结\n\n---\n\n## 菜品简介\n### 四川传统名菜\n- **起源**: 川菜代表作之一，以其独特的酸甜口味著称。\n- **特点**:\n  - 红亮色泽\n  - 嫩滑口感\n- **所需工具**:\n  - 炒锅\n  - 刀具\n  - 砧板\n\n---\n\n## 材料清单\n### 主料\n- 猪里脊肉 200g\n- 黑木耳 5朵\n- 胡萝卜 半根\n- 青椒 半个\n\n### 辅料\n- 生姜 几片\n- 大蒜 几瓣\n- 小葱 适量\n\n### 调料\n- 白糖 一大勺\n- 醋 一大勺\n- 生抽 一小勺\n- 老抽 少许\n- 水淀粉 适量\n\n---\n\n## 前期准备\n### 肉处理\n1. 将猪里脊切成细丝。\n2. 加入少许盐和水淀粉腌制约10分钟。\n\n### 蔬菜处理\n- 黑木耳提前泡发后切丝。\n- 胡萝卜去皮切丝；青椒去籽切丝。\n\n### 调味汁配制\n- 混合白糖、醋、生抽、老抽以及适量水淀粉制成酱汁备用。\n\n---\n\n## 烹饪步骤\n1. 盘中倒入适量油，开中火加热至温热。\n2. 先下干辣椒段与姜蒜末爆香。\n3. 接着加入腌好的肉丝快速翻炒至变色后盛出。\n4. 在同一锅内依次加入胡萝卜丝、黑木耳丝及青椒丝继续翻炒。\n5. 当蔬菜略微软化时，倒入之前调好的酱汁，转大火快速翻拌均匀收汁。\n6. 最后撒上切好的葱花即可出锅装盘。\n\n---\n\n## 小贴士\n- 使用里脊肉可以让菜肴更加嫩滑。\n- 水淀粉的最佳比例为1:3（水：淀粉）。\n- 可根据个人口味调整糖与醋的比例，通常建议保持在1:1左右作为基础。\n\n---\n\n## 结束语\n### 关键要点\n- 成功的关键在于掌握好火候与酱汁调配的比例。\n- 如果您喜欢这道菜，请不要忘记关注我的微信公众号[账号]获取更多美食教程！\n"
}
## 示例返回
输出物：
{
    "download_url": "http://< your ip or domain >:< port >/download/< files name >.pptx",
    "filename": "< files name >.pptx"
}
## 服务说明
- 镜像服务将Marp格式的PPT转换为PPTX
- 每日限制20次调用
- 如需更多调用次数，请联系开发者

## 版权声明
本项目受版权保护，任何个人或组织可下载、试用本项目；
获取源码请联系作者。

## 使用条款
如须商用或修改本项目必须：
1. 获得作者的书面许可
2. 支付相应的使用费用
未经授权，禁止将本项目用于任何商业用途。如需商业使用，请联系作者获取许可。

## 联系方式
作者：[mir.q]  
邮箱：[qjqb1@sina.com]
