# CTF Pwn 可视化学习平台

一个通过交互式可视化帮助学习 CTF Pwn（二进制漏洞利用）的平台。

## 学习路径

### 0. 汇编基础 (0基础入门)

| 模块 | 内容 |
|------|------|
| [汇编基础](pages/asm-basics.html) | 寄存器、内存模型、栈概念 |
| [指令详解](pages/asm-instructions.html) | MOV/LEA/ADD/SUB/JMP/CALL等 |
| [函数调用约定](pages/asm-calling-convention.html) | x64 Linux/Windows 调用约定 |
| [实战分析](pages/asm-practice.html) | C代码对照汇编分析 |

### 1. Pwn 漏洞利用

| 模块 | 难度 | 内容 |
|------|------|------|
| [栈溢出原理](pages/stack-overflow.html) | 入门 | 函数序言、gets溢出 |
| [格式化字符串](pages/format-string.html) | 入门 | %s/%x/%n等格式说明符 |
| [ROP链构造](pages/rop.html) | 进阶 | gadgets拼接、DEP绕过 |
| [堆内存管理](pages/heap-basic.html) | 进阶 | glibc堆分配器原理 |
| [Fastbin Attack](pages/fastbin-attack.html) | 高阶 | double-free、fd指针 |
| [栈迁移](pages/stack-pivot.html) | 高阶 | leave指令、栈控制权 |

## 快速开始

```bash
# Python 3
cd pwn-learning
python -m http.server 8080

# 然后访问 http://localhost:8080
```

## 推荐学习顺序

```
汇编基础 → 栈溢出 → 格式化字符串 → ROP → 堆基础 → Fastbin Attack → 栈迁移
```

## 项目结构

```
pwn-learning/
├── index.html              # 主页
├── pages/
│   ├── asm-basics.html     # 汇编基础
│   ├── asm-instructions.html# 指令详解
│   ├── asm-calling-convention.html # 函数调用约定
│   ├── asm-practice.html   # 实战分析
│   ├── stack-overflow.html # 栈溢出
│   ├── format-string.html  # 格式化字符串
│   ├── rop.html           # ROP
│   ├── heap-basic.html    # 堆基础
│   ├── fastbin-attack.html# Fastbin
│   └── stack-pivot.html   # 栈迁移
└── README.md
```

## 技术栈

- Tailwind CSS
- Lucide Icons
- 纯 JavaScript (无需构建)

## 许可证

MIT License
