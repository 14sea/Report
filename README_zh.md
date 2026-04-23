# Report

两个虚拟机逃逸方面的漏洞复现报告。

## 报告列表

| 漏洞编号 | 目标平台 | 逃逸方式 | 报告链接 |
|----------|----------|----------|----------|
| CVE-2015-3456 | QEMU/KVM (VENOM) | 软盘控制器缓冲区溢出，覆盖 `qemu_set_irq` 的 handler 指向 `system`，实现宿主机任意命令执行 | [CVE-2015-3456.md](CVE-2015-3456.md) |
| CVE-2018-2844 | VirtualBox | VDMA 命令处理中的 TOCTOU 竞态条件，利用二级跳转表劫持控制流执行 shellcode | [CVE-2018-2844.md](CVE-2018-2844.md) |

## 环境信息

- **CVE-2015-3456**: CentOS 7.9 宿主机 + QEMU 1.5.3 + Debian Squeeze 虚拟机
- **CVE-2018-2844**: Ubuntu 16.04 宿主机 + VirtualBox 5.2.6 + Ubuntu 16.04 Server 虚拟机

## 目录结构

```
.
├── README.md
├── CVE-2015-3456.pdf          # 原始 PDF 报告
├── CVE-2015-3456.md           # Markdown 版报告
├── CVE-2018-2844.pdf          # 原始 PDF 报告
├── CVE-2018-2844.md           # Markdown 版报告
└── resources/                 # 报告中引用的截图
    ├── CVE-2015-3456_img*.png
    └── CVE-2018-2844_img*.png
```
