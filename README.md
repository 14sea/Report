# VM Escape Vulnerability Reports

Two vulnerability reproduction reports on virtual machine escape techniques.

## Reports

| CVE | Target | Escape Method | Report |
|-----|--------|---------------|--------|
| CVE-2015-3456 | QEMU/KVM (VENOM) | FDC FIFO buffer overflow, overwriting `qemu_set_irq` handler to call `system`, achieving arbitrary command execution on host | [English](CVE-2015-3456.md) / [Chinese](CVE-2015-3456_zh.md) |
| CVE-2018-2844 | VirtualBox | TOCTOU race condition in VDMA command processing, hijacking control flow via indirect jump table to execute shellcode | [English](CVE-2018-2844.md) / [Chinese](CVE-2018-2844_zh.md) |

## Environment

- **CVE-2015-3456**: CentOS 7.9 host + QEMU 1.5.3 + Debian Squeeze guest
- **CVE-2018-2844**: Ubuntu 16.04 host + VirtualBox 5.2.6 + Ubuntu 16.04 Server guest

## Directory Structure

```
.
├── README.md                  # English README
├── README_zh.md               # Chinese README
├── CVE-2015-3456.md           # English report
├── CVE-2015-3456_zh.md        # Chinese report
├── CVE-2018-2844.md           # English report
├── CVE-2018-2844_zh.md        # Chinese report
├── backup/                    # Original PDF reports
│   ├── CVE-2015-3456.pdf
│   └── CVE-2018-2844.pdf
└── resources/                 # Screenshots referenced in reports
    ├── CVE-2015-3456_img*.png
    └── CVE-2018-2844_img*.png
```
