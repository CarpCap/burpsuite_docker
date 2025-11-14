
# 🚀 BurpSuite Docker 批量部署 

选择语言 / Select Language:

- [中文](README_zh.md)
- [English](README.md)


本项目可以在 Docker 环境中启动 **多个 Burp Suite 实例**，支持 GUI 和无 GUI 模式。

当前版本：**Burp Suite 2020.11.3**

---

## 使用场景：

- 批量扫描
- 流量转发
- 爬虫后台
- 云服务器大规模部署


---

## 📁 镜像配置

Burp Suite Docker 镜像的默认配置文件路径：
``/usr/local/docker/burp/space/files/default.json``

你可以替换此文件来自定义 Burp Suite 配置，例如代理设置、证书或插件。

---

## 🖥 GUI 模式

适用于需要操作界面的场景。

### 前置要求：

- 准备 X11 服务器（例如 MobaXterm ）
- 配置 DISPLAY 环境变量（示例：`127.0.0.1:0.0`）

**Docker Run：**

```bash
docker run -di --name burp-gui \
  -e JAVA_OPTS='-Xmx2g' \
  -e DISPLAY=127.0.0.1:0.0 \
  carpcap/burpsuite-gui:2020.11.3
```


## 🧰 无 GUI 模式
适用于服务器批量部署，可节省 GUI 消耗的资源（CPU / 内存）。
```bash
docker run -di --name burp-nogui \
  -e JAVA_OPTS='-Xmx2g' \
  carpcap/burpsuite:2020.11.3
```

