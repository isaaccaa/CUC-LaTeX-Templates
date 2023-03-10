# 中国传媒大学考研/夏令营/推免/申博材料非官方LaTeX模板

此模板为中国传媒大学考研/夏令营/推免/申博材料的民间自制LaTeX模板，与官方Word模板有99.9%的相似度，供习惯LaTeX写作、追求更漂亮排版效果的同学使用。

## ⚠️ 重要提醒

* 本模板未经学校相关部门审核及授权，使用前请务必斟酌。
* 考生提交的文档应当以[中传研招](https://yz.cuc.edu.cn/)提供的官方文档模板为准，模板详见报名系统。如本模板与报名系统模板有出入，应以**报名系统**的内容为准。
* 请考生使用本模板时仔细确认导出的pdf是否与官方提供的模板内容一致、格式统一！
* 任何由于使⽤本模板⽽引起的问题均与本模板作者⽆关。

## 模板介绍

[示例文档源码](example.tex)，[文档效果](example.pdf)

### 模板选择

本模板包含以下6种模板，通过在导言区的 `\setup` 中设置 `Type` 字段来选择要渲染的模板：

| Type | 考生类别                     | 文档简称   | 文档全称                                           |
| ---- | ---------------------------- | ---------- | -------------------------------------------------- |
| 0    | 考研                         | 个人陈述   | 报考攻读硕士学位研究生个人陈述                     |
| 1    | 考研                         | 科研设想   | 报考攻读硕士学位研究生科研设想或专业实践计划       |
| 2    | 申请博士(普通招考、硕博连读) | 申请信     | 报考攻读博士学位研究生申请信                       |
| 3    | 申请博士(普通招考、硕博连读) | 研究计划书 | 拟攻读博士学位的研究计划书                         |
| 4    | 参加我校夏令营               | 个人陈述   | 20XX年优秀大学生夏令营个人陈述                     |
| 5    | 推免硕士(含直博)             | 个人陈述   | 招收推荐免试攻读硕士学位研究生（含直博生）个人陈述 |

使用时仅需将默认的 `Type = 0` 注释掉，将需要使用的模板行取消注释即可

### 设置页码编号、标题名

对于考研、申请博士的同学，由于需要提交一组申请材料，并在**报考材料清单目录**中从头到尾依次编号，可将 `StartPage = 1` 改为自己所需的数值，将从这个数字开始对页码进行编号。如改为`10`，则第一页的页码即为`10`。

对于参加我校夏令营的同学，个人陈述的标题中含有年份，因此可将 `Title` 改为研招网提供的Word模板中的标题，在生成标题时会按照输入的字符串进行文档的生成。其他考生可以无视这一选项。

### 使用方法

编译引擎为 `xelatex` 


```tex
% 选择文档类别，这里使用伪粗体可以实现仿宋字体的加粗
\documentclass[AutoFakeBold]{ApplytoCUC}

\setup{.....}

% 在正文中使用 \ApplyCUC ，并在其中输入内容即可
\begin{document}
\ApplyCUC{
    % ================= 要填写的正文内容 =================
    ...
    % ================= 要填写的正文内容 =================
}
\end{document}
```

祝大家一切顺利！