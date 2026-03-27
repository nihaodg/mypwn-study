# CTF Pwn 可视化学习平台

一个通过交互式可视化帮助学习 CTF Pwn（二进制漏洞利用）的平台。

## 特性

- **栈溢出原理** - 深入理解函数序言、栈帧结构以及缓冲区溢出
- **格式化字符串漏洞** - 探索 printf 系列函数的格式说明符威力
- **ROP 链构造** - 学习通过拼接 gadgets 构建攻击载荷
- **堆内存管理** - 理解 glibc 堆分配器的内部工作原理
- **Fastbin Attack** - 掌握堆漏洞利用技术
- **栈迁移** - 学习在受限环境下控制栈空间

## 快速开始

### 方式一：直接打开 HTML

```bash
# 使用浏览器直接打开
open pwn-learning/index.html
# 或
firefox pwn-learning/index.html
```

### 方式二：启动本地服务器

```bash
# Python 3
cd pwn-learning
python -m http.server 8080

# Node.js (npx)
npx serve pwn-learning

# PHP
php -S localhost:8080 -t pwn-learning
```

然后访问 http://localhost:8080

## 项目结构

```
pwn-learning/
├── index.html              # 主页
├── pages/
│   ├── stack-overflow.html # 栈溢出原理
│   ├── format-string.html  # 格式化字符串漏洞
│   ├── rop.html            # ROP 链构造
│   ├── heap-basic.html     # 堆内存管理基础
│   ├── fastbin-attack.html # Fastbin Attack
│   └── stack-pivot.html    # 栈迁移
└── README.md
```

## 技术栈

- Tailwind CSS - 样式框架
- Lucide Icons - 图标库
- 纯 JavaScript - 无需构建工具

## 学习路径

1. 栈溢出原理 (入门)
2. 格式化字符串漏洞 (入门)
3. ROP 链构造 (进阶)
4. 堆内存管理基础 (进阶)
5. Fastbin Attack (高阶)
6. 栈迁移 (高阶)

## 贡献

欢迎提出建议和改进意见！

## 许可证

MIT License
