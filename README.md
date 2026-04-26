# V2Ray 一键安装脚本

![Shell](https://img.shields.io/badge/language-Shell-orange?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)

> 基于 [233boy/v2ray](https://github.com/233boy/v2ray) 优化 fork，修复安全漏洞并改进 Shell 最佳实践。

---

## 与原版的区别

在原版 233boy/v2ray 基础上做了以下改进：

- **安全加固**: 修复命令注入、路径遍历、未验证下载等安全问题
- **Shell 规范**: 变量引用加引号、`set -euo pipefail`、错误处理改进
- **下载可靠性**: 增加 checksum 校验和重试机制

---

## 快速安装

```bash
bash <(curl -sL https://raw.githubusercontent.com/AzurePath749/v2ray/master/install.sh)
```

安装完成后，输入 `v2ray` 即可管理。

---

## 管理命令

```
v2ray info          查看 V2Ray 配置信息
v2ray config        修改配置
v2ray link          获取 V2Ray 链接
v2ray qr            获取二维码
v2ray status        查看运行状态
v2ray start         启动 V2Ray
v2ray stop          停止 V2Ray
v2ray restart       重启 V2Ray
v2ray uninstall     卸载 V2Ray
```

---

## 支持的传输协议

| 协议 | 说明 |
|------|------|
| TCP  | 默认，兼容性最好 |
| WebSocket | 需要 Web 服务器 |
| HTTP/2 | 需要 TLS 证书 |
| mKCP | UDP 传输，抗丢包 |
| QUIC | 基于 UDP |
| KCP | UDP 传输 |

---

## 支持的系统

- Debian 8+
- Ubuntu 16+
- CentOS 7+
- Fedora

---

## 致谢

- 原作者 [233boy](https://github.com/233boy)
- [V2Ray 官方文档](https://www.v2ray.com/)
- [原版搭建教程](https://github.com/233boy/v2ray/wiki)

## License

MIT
