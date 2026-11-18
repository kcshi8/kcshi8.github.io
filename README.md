# Kecheng Shi 的个人主页

主页地址是 [kcshi8.github.io](https://kcshi8.github.io/)。在 GitHub 网页上就可以编辑。打开下表中的文字文件，点铅笔图标，修改后点 **Commit changes**，将改动提交到 `main`。GitHub Pages 会自动重新发布。

| 想修改的内容 | 对应文件 |
| --- | --- |
| 姓名、职位、导师及其主页、首页简介、研究问题、学术背景、邮箱、学术档案链接、摄影署名 | [个人资料](_data/profile.yml) |
| 论文标题、作者、年份、会议、ePrint、分组与排序 | [论文列表](_data/papers.yml) |
| Conference subreviewing 的年份和会议 | [Service 栏目](_includes/service.md)，每个年份一行 |
| 个人爱好、FIDE 主页、等级分和游戏段位 | [Personal 栏目](_includes/personal.md)，直接修改文字即可。每项游戏单独一行，以 `- ` 开头 |
| 颜色、字号、间距和手机布局 | [样式表](assets/style.css) |
| CV 或照片 | 在 [assets 文件夹](assets/) 中通过 **Add file → Upload files** 上传同名的 `Kecheng-Shi-CV.pdf` 或 `kecheng-shi.jpg`；换文件名时也更新个人资料中的路径 |
| 顶部导航、板块顺序 | [index.html](index.html) 里的导航及 `main` 中的板块顺序 |
| 某个板块的 HTML 排版 | [_includes 文件夹](_includes/)，每个文件对应一个板块 |

## 添加或更新论文

在 `_data/papers.yml` 中找到对应分组，复制其中一篇作品的条目，保持原缩进。下面展示一个合著手稿的写法。

```yaml
    - title: "Paper title"
      venue: Manuscript
      coauthors:
        - First Coauthor
        - Second Coauthor
```

- `coauthors` 只填合作者，按文章署名顺序排列。页面会自动显示 “with First Coauthor and Second Coauthor”。独著直接省略 `coauthors`。
- 有 ePrint 后，复制同组已有论文的 `links` 段并替换网址。标题会链接至第一项。尚无公开版本时省略整个 `links` 段。
- `year` 和 `summary` 都可以省略。标题含冒号时用双引号括起来。
- 页面沿用文件中的排列顺序。移动整个论文条目即可调整组内顺序。移动整个分组即可改变首页标签和论文分组的顺序，第一组会突出显示。

## 检查发布

提交后可在仓库的 **Actions** 标签页查看 **pages build and deployment**。部署完成后刷新公开主页。GitHub 保留每次提交，旧版可在仓库历史中查看。
