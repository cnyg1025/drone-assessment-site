# YANG AI STUDIO · 产品官网（落地页）

> 开源低空智能评估平台的产品介绍页：灾后定损、环境监测、生态巡护。
> 单文件静态站点，零构建、零依赖服务端。

- 在线访问：<https://cnyg1025.github.io/drone-assessment-site/>
- 交互演示：<https://cnyg1025.github.io/drone-app-demo/>

## 特点

- **单文件**：所有结构、样式、文案（中/EN/FR 三语）都在 `index.html` 内
- **零后端**：转化入口为邮件（`mailto:`），无需表单服务
- **可直接部署**：任何静态托管（GitHub Pages / OSS / Nginx）均可

## 本地预览

```bash
python -m http.server 8000
# 打开 http://localhost:8000/
```

## 目录

```
index.html          唯一页面（含三语文案与交互脚本）
assets/             站点使用的图片
```

## 修改指引

| 想改什么 | 改哪里 |
| --- | --- |
| 文案 | `index.html` 中 `data-i18n` 对应元素，或底部 `I18N` 字典 |
| 指标数字 | 搜索 `data-target` |
| 联系方式 | 搜索 `mailto:` |
| 配色 | `<script>` 中 `tailwind.config` 与 `<style>` 段 |

> **样式已本地化**：原先依赖 `https://cdn.tailwindcss.com`（浏览器端实时编译），现改为仓库内的预编译 `tailwind.css`（约 16 KB），页面不再有第三方单点依赖。
>
> 如果新增或修改了 Tailwind 类名，需要重新生成样式：
>
> ```bash
> npx tailwindcss@3 -i /dev/null -o tailwind.css --content index.html --minify
> ```
>
> 或临时把 `tailwind.css` 换回 CDN 的 `<script>` 采一次样式，再换回 `<link>`。

## 许可

[Apache License 2.0](LICENSE) © 2026 YANG AI STUDIO
