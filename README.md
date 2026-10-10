# NAS测速

<p align="center">
  <img src="logo.png" alt="NAS测速" width="180" />
</p>

一款 [飞牛OS（fnOS）](https://www.fnnas.com/) 网速测试应用，支持测试 **本机与 NAS 之间的 fn 连接速度**，以及 **NAS 到互联网的外网带宽**。

## ✨ 功能特性

- **fn 内网测速**：测试浏览器所在设备与飞牛 NAS 之间的连接速度
- **外网带宽测速**：测试 NAS 到互联网的上传 / 下载带宽
- **10 个外网测速节点**：内置中科大 USTC、Cloudflare、清华 TUNA、上海交大等节点
  - 自动探测节点延迟，智能选择最快节点
  - 支持手动指定节点，并可单独测量节点延迟
- **上传 / 下载通道自动解耦**：所选节点不支持上传时，自动切换 Cloudflare 上传通道
- **多线程测速**：下载 / 上传均支持多线程并发
- **延迟与抖动测量**：实时显示延迟（Ping）与抖动（Jitter）
- **实时仪表盘**：基于 ECharts 的动态速度曲线与仪表盘
- **测速历史记录**：保留历史测速结果，方便对比
- **亮色 / 深色主题**：跟随切换，夜间使用更舒适

## 📦 安装

1. 前往 [Releases](https://github.com/pdf-covert/speed-test/releases) 下载对应架构的安装包：
   - `speedtest_v1.0.0_x86.fpk` —— x86 架构
   - `speedtest_v1.0.0_arm.fpk` —— ARM 架构
2. 打开飞牛 OS 的 **应用中心 → 手动安装**，选择下载的 `.fpk` 文件完成安装
3. 安装完成后，在桌面打开「NAS测速」即可开始测速

## 🚀 使用说明

1. **fn 内网测速**：打开应用后点击开始，即可测量当前设备与 NAS 之间的连接速度
2. **外网测速**：应用会自动探测各节点延迟并选择最快的节点；也可以在节点列表中手动选择，或单独测试某个节点的延迟
3. 测速过程中可实时查看速度曲线、延迟与抖动数据
4. 测速结果会自动保存到历史记录中

## 🔧 从源码构建

依赖：[fnpack](https://developer.fnnas.com/)（飞牛官方打包工具）、Go 1.x

```bash
git clone <本仓库>
cd speed-test
./build.sh
```

构建脚本会自动交叉编译 arm / x86 两个架构的 `speedtest-server`，并分别打包为 `.fpk` 输出到 `dist/` 目录。

## 📄 项目信息

- **开发者 / 发布者**：[pdf-covert](https://github.com/pdf-covert)
- **应用分类**：第三方应用（fnOS App Center）
- **当前版本**：v1.0.0
