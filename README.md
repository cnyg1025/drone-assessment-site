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

> ⚠️ 当前样式依赖 `https://cdn.tailwindcss.com`（浏览器端编译）。若目标用户在中国大陆，建议改为预编译 CSS——见整改清单 P0-2。

## 许可

[Apache License 2.0](LICENSE) © 2026 YANG AI STUDIO
