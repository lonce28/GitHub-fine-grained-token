# 上线与搜索引擎收录说明

## 结论

当前网站只是本地文件，地址以 `file://` 开头，搜索引擎无法收录。要让百度、360、搜狗、Google 等搜索引擎搜到，必须先部署到公网 URL。

## 推荐免费部署方式

### 方案 A：GitHub Pages

免费地址格式：

```text
https://你的用户名.github.io/GitHub-fine-grained-token/
```

适合长期维护、文章持续更新、后续绑定独立域名。

### 方案 B：Cloudflare Pages

免费地址格式：

```text
https://engineering-tech-blog.pages.dev/
```

适合静态站点，访问速度和免费额度都比较友好。

## 上线后必须替换的文件

上线拿到真实网址后，把下面两个文件里的示例地址替换为真实地址：

- `robots.txt`
- `sitemap.xml`

例如真实网址是：

```text
https://engineering-tech-blog.pages.dev/
```

则 `robots.txt` 里应改成：

```text
Sitemap: https://engineering-tech-blog.pages.dev/sitemap.xml
```

`sitemap.xml` 里的所有 `https://lonce28.github.io/GitHub-fine-grained-token/` 也要改成真实网址。

## 搜索引擎提交

上线后建议提交：

- 百度搜索资源平台：提交首页和 `sitemap.xml`
- 360站长平台：提交首页
- 搜狗资源平台：提交首页
- Bing Webmaster Tools：提交 `sitemap.xml`

## 百度收录注意

百度通常不会“立刻搜到”。新站常见流程是：

1. 公网可访问
2. 页面标题、描述、正文内容完整
3. `robots.txt` 允许抓取
4. `sitemap.xml` 地址正确
5. 主动提交到百度搜索资源平台
6. 等待抓取和放出索引

时间可能从几天到数周不等。工程行业垂直内容建议持续发布原创文章，优先做长尾关键词，如“天然气管道焊接质量控制”“站场施工HSE检查表”“工程竣工资料编制流程”。
