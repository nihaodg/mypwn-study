# CTF Pwn 可视化学习平台

一个通过交互式可视化帮助学习 CTF Pwn（二进制漏洞利用）的平台。

## 学习路径

### 0. 汇编基础 (0基础入门)

| 模块 | 内容 |
|------|------|
| [汇编基础](pages/asm-basics.html) | 寄存器、内存、栈概念 |
| [指令详解](pages/asm-instructions.html) | MOV/LEA/ADD/SUB/JMP/CALL等 |
| [函数调用约定](pages/asm-calling-convention.html) | x64 Linux/Windows 调用约定 |
| [实战分析](pages/asm-practice.html) | C代码对照汇编分析 |

### 1. GDB 调试学习

| 模块 | 内容 |
|------|------|
| [GDB教程](pages/gdb-learning.html) | 常用命令、速查表、实战调试 |
| [Pwn函数](pages/pwn-functions.html) | Pwntools函数详解、使用场景、输出示例 |

### 2. Pwn 漏洞原理

| 模块 | 难度 | 内容 |
|------|------|------|
| [栈溢出原理](pages/stack-overflow.html) | 入门 | 函数序言、gets溢出 |
| [格式化字符串](pages/format-string.html) | 入门 | %s/%x/%n等格式说明符 |
| [ROP链构造](pages/rop.html) | 进阶 | gadgets拼接、DEP绕过 |
| [堆内存管理](pages/heap-basic.html) | 进阶 | glibc堆分配器原理 |
| [Fastbin Attack](pages/fastbin-attack.html) | 高阶 | double-free、fd指针 |
| [栈迁移](pages/stack-pivot.html) | 高阶 | leave指令、栈控制权 |

### 3. CTF-Pwn 实战演练

| 模块 | 题目数 | 内容 |
|------|--------|------|
| [CTF实战首页](pages/ctf-index.html) | 12道 | 源码+gcc编译+Python脚本 |
| [栈溢出CTF](pages/ctf-stack-overflow.html) | 3道 | gets溢出、变量篡改 |
| [格式化字符串CTF](pages/ctf-format-string.html) | 3道 | 内存泄露、%n写入 |
| [ROP CTF](pages/ctf-rop.html) | 3道 | ret2libc、gadgets |
| [堆漏洞CTF](pages/ctf-heap.html) | 3道 | UAF、Double Free |

## 快速开始

```bash
cd pwn-learning
python -m http.server 8080
# 然后访问 http://localhost:8080
```

## 推荐学习顺序

```
汇编基础 → 栈溢出 → 格式化字符串 → ROP → 堆基础 → Fastbin Attack → 栈迁移
                    ↓
               CTF实战演练 (理论+实践)
```

## 项目结构

```
pwn-learning/
├── index.html              # 主页
├── pages/
│   ├── asm-basics.html     # 汇编基础
│   ├── asm-instructions.html# 指令详解
│   ├── asm-calling-convention.html
│   ├── asm-practice.html
│   ├── gdb-learning.html  # GDB调试学习
│   ├── pwn-functions.html  # Pwn脚本函数
│   ├── stack-overflow.html
│   ├── format-string.html
│   ├── rop.html
│   ├── heap-basic.html
│   ├── fastbin-attack.html
│   ├── stack-pivot.html
│   ├── ctf-index.html      # CTF实战首页
│   ├── ctf-stack-overflow.html
│   ├── ctf-format-string.html
│   ├── ctf-rop.html
│   └── ctf-heap.html
└── README.md
```

## CTF实战使用方法

每个CTF题目页面包含：

1. **C/C++源码** - 带有详细注释的源代码
2. **漏洞分析** - 标注漏洞点和利用方法
3. **gcc编译命令** - 可直接复制使用
4. **Python解题脚本** - 使用pwntools编写的完整exploit
5. **脚本注释** - 解释每个步骤的含义

## 常用工具

- **pwntools** - Python漏洞利用框架
- **gdb + pwndbg** - 调试器
- **ROPgadget** - 搜索gadgets
- **checksec** - 检查二进制保护

## 技术栈

- Tailwind CSS
- Lucide Icons
- 纯 JavaScript (无需构建)

## 许可证

MIT License
