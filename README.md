# Skill-Hut
- A total of 316 skills across 11 categories: Reverse Engineering (14), Decompilation/Disassembly (38), Cryptography (26), Decryption/Cracking (29), Malware Analysis (47), Steganography (30), Obfuscation/Deobfuscation (21), Digital Forensics (23), Binary Analysis (20), CTF Tools (35), and Unpacking/Deconstruction (33).
关于「荒天帝的奶酪」· 详细说明
这是一个单一自包含的安全技能一体化面板。所有内容（技能数据 + 构建脚本源码）都已内嵌在这一个 HTML 文件里，无需联网、无需额外依赖，双击即可在浏览器打开。本页同时提供中文 / 英文一键互换。

一、面板涵盖的内容
技能小屋：从 GitHub 按 star 热度精选的 316 个安全相关仓库，分 11 个分类（逆向工程、反编译/反汇编、加密、解密/破密、恶意代码分析、隐写术、混淆/反混淆、数字取证、二进制分析、CTF 工具、脱壳/拆解），支持关键词搜索与分类筛选。

源码文件：本面板的数据集 skills_data.json，以及生成它的三个源码文件 fetch_github.py、build_site.py、validate.js，均可在面板内直接查看、复制。

二、内嵌文件详细说明
index.html — 面板本体。一个自包含的 HTML 文件，内含技能数据（316 个 GitHub 仓库）与全部构建脚本源码，带搜索、分类筛选、弹窗详情、源码查看、语言切换功能。
skills_data.json — 底层数据集。记录从 GitHub 按 star 热度精选的 316 个安全相关仓库的结构化信息：名称、全名、描述、链接、star 数、语言、话题标签、分类。是面板的唯一数据源。
fetch_github.py — 数据采集脚本。通过 GitHub 公开搜索 API，按 12 个安全主题（逆向工程、恶意代码分析、密码学、隐写术、数字取证、二进制分析、CTF、密码破解、代码混淆、脱壳、反编译、反汇编）抓取仓库，去重后写出 skills_data.json。
build_site.py — 网页生成脚本。读取 skills_data.json，按关键词规则把仓库校准分类，过滤低质量项（star<100），格式化 star 数，生成带「小屋」主题的交互式 index.html。
validate.js — 校验脚本。解析面板内联 JSON，确认数据块、链接合法性、源码内嵌完整性。
build_panel.py — 一体化面板生成器（本文件由它产出）。读取数据集与三个源码文件，将它们全部内嵌进最终的 index.html，并生成「源码文件」「关于」标签页。
三、使用方法
搜索：在搜索框输入关键词（仓库名 / 描述 / 标签，支持中英文），实时过滤。

筛选：点击顶部分类标签，只看某一类技能。

详情：点击任意卡片，弹出该仓库的描述、标签、语言、star 与 GitHub 直达链接。

源码：切换到「源码文件」页，可查看并复制面板用到的全部脚本。

语言：点击右上角「EN / 中」按钮，界面在中文与英文之间切换（偏好会记住）。

四、数据来源
数据来自 GitHub 公开仓库搜索 API，抓取于 2026-10-16。所有链接均指向 github.com 原仓库。

五、合规声明
本面板仅用于合法授权的安全研究、学习与教学。请确保在你自己拥有或已获书面授权的系统/软件上进行任何逆向、加解密或分析操作，遵守所在地法律法规。
