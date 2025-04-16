# AutoFisher-VRC 🎮⚡

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![OSC Protocol](https://img.shields.io/badge/OSC-1.1-brightgreen)](https://opensoundcontrol.stanford.edu/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

自动钓鱼

读取日志+OSC输入控制，合法辅助，可完全后台的挂机脚本

![image](https://github.com/user-attachments/assets/53213bee-c6dd-4d24-8551-0ced09c8f99e)

使用方法：https://www.bilibili.com/video/BV1TqotYrEDe

[exe版本下载](https://github.com/arcxingye/AutoFisher-VRC/releases/download/exe/autofish.exe) 【exe通过Nuitka打包难免报毒，不放心的可以下py文件运行】

说明

蓄力时间：抛竿蓄力多少秒

休息时间：上一轮钓鱼到下一轮钓鱼的间隔

超时重钓：超过多少分钟没上鱼则重新进行钓鱼

## 开发说明

### 自动构建与发布

本项目使用GitHub Actions自动构建Windows可执行文件：

- 当代码推送到main或master分支时，会自动触发构建
- 构建使用Nuitka将Python代码打包为独立的Windows可执行文件
- 构建完成后会自动创建GitHub Release，并上传exe文件和包含所有依赖的zip文件

如果您想要手动构建，可以使用以下命令：

```bash
pip install nuitka python-osc watchdog
python -m nuitka --standalone --windows-disable-console --follow-imports AutoFisher.py
```
