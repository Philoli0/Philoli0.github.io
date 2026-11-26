# 清如AI 教学工作台

面向经管课程，把材料导入、资料课堂、数字讲师精讲、动态推演、理解练习与原文追问放在同一学习路径中。

## 网页入口

- index.html：教学工作台，导入材料和继续学习。
- courses.html：课程库，筛选精讲、资料课堂与本地草稿。
- classroom.html：市场均衡精品课，完整数字讲师视频、供求图与蛛网推演、5道练习、6组预制语音答疑。
- classroom.html?course=microeconomics：《微观经济学》完整资料课堂，722页、127单元、53组练习，保留1350个原文块及图表。
- classroom.html?course=business-topics：经管应用专题资料课堂，120页、24单元、24组练习。
- research.html：方法链路、成片检查和保留测量记录的组件对照。

## 材料导入

支持DOCX、PPTX、带文字层PDF、TXT和Markdown，每份不超过20MB、一次最多8份。浏览器内提取文字和DOCX表格、插图，按文档标题层级组织课堂草稿，并保留完整来源；不向服务器上传材料。可粘贴文字、导出.qingru.json课堂包，在另一浏览器重新导入。

草稿保存在当前浏览器的IndexedDB。清除浏览器数据会清除本地草稿，建议导出保留。原文核对题与小结使用规则和摘录编排，开放式大模型问答与新人物视频生成需要完整本地服务。本静态网页不会在导入后调用GPU或假装已经生成新的视频。

新材料本次提供资料课件草稿；已有精品课使用已完成媒体。视频制作仍暂停，已有声音与人物媒体未改动。

## 运行与发布

推荐通过HTTP/HTTPS访问，使用Chrome或Edge。GitHub Pages目标地址为 https://Philoli0.github.io/ ，是否上线以发布状态和实际访问为准。

离线可直接打开index.html，使用内置课程与DOCX/PPTX/TXT导入。PDF使用浏览器模块与Worker，请通过HTTP/HTTPS地址导入。使用项目中tools/serve_midterm.py可启动本地预览，地址http://127.0.0.1:8789/；该脚本已为.mjs和.wasm配置正确MIME类型。

完整目录可部署到GitHub Pages，无需API密钥。github-source为准备好的发布仓库；publish-github.ps1会提交和推送到Philoli0/Philoli0.github.io，并配置main分支根目录的Pages。

## 来源与范围

人物基于EchoMimic V2；声音采用固定参考的Qwen3-TTS；教学场景组织参考OpenMAIC。平台实现材料可追溯编排、音画同轨播放、动态交互图表和结果验收。网页文件解析使用fflate 0.8.2（MIT）与PDF.js 6.5.438（Apache-2.0），许可随vendor目录提供。详见credits.html。
