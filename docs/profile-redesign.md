# 青绿山海 · 主页设计与维护

更新日期：2026-10-16。

## 设计

把个人主页编排成一卷当代青绿山水：黛青底色、石绿山峦、绢金线条与朱砂印章。横幅题字「以码为舟，山海可渡」，正文保留 GitHub 原生可访问文字与链接，在深浅主题下都可阅读。

阅读顺序为个人定位、最新项目 classroom-annotator、全栈竞赛作品与论文研究、简历开源、竞赛荣誉和交流入口。工程和研究事实沿用现有主页或对应仓库的公开说明，不虚构成绩或功能。

视觉素材全部存放在仓库中，不依赖外部统计卡片或图片服务。SVG 不包含脚本、外链图片或 foreignObject；主要中文转为路径以稳定显示，源文件保留可编辑文字。轻微装饰动画支持减少动态效果偏好。

## 实施与验收约定

- 保存现有 main 到远端备份分支，并核对提交一致。
- 核对 classroom-annotator 的 README、功能与链接。
- 制作原创山水横幅与项目视觉，更新 README。
- 检查 SVG、所有本地引用、项目链接与原有重要内容。
- 渲染图形在 1280 和 360 像素宽度下的效果，使用 GitHub GFM 接口检查正文编排，并进行独立审阅。
- 验证后提交并发布主页，核对远端文件与版本。

此项为可逆的主页文案与图形更新，以静态检查和真实渲染验证，不引入应用测试框架。

## 旧版与回退

改版前完整版本：[`backup/profile-before-guofeng-2026-10-16`](https://github.com/XB-Dong/XB-Dong/tree/backup/profile-before-guofeng-2026-10-16)。

原始提交：`4171caab15a978ae1936804eacd30825b2e2bcfb`。备份分支包含原 README 和原横幅。

如需恢复旧版，在一次新的提交中恢复该版本的 README 即可，不需要重写历史：

```sh
git fetch origin
git switch main
git pull --ff-only
git restore --source=origin/backup/profile-before-guofeng-2026-10-16 -- README.md assets/ink-profile-banner.svg
git add README.md assets/ink-profile-banner.svg
git commit -m "Restore profile before the 2026-10-16 redesign"
git push origin main
```

## 编辑视觉

`assets/src/` 保存可编辑 SVG，`assets/` 中对应 SVG 为实际展示文件。修改源文件后，用 Inkscape 的「文本转路径」SVG 导出功能重新生成展示文件，再检查一次渲染效果。所有文案也保留在 README 中，图片不能取代项目链接与说明。
