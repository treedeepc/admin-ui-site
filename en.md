> Runlume · admin design baseline
# Admin Design

The standard admin template extracted from the Runlume platform frontend: semantic tokens, app shells, shared components and standard pages. Plug in your own menu, identity and APIs.

## 能力

- **Semantic token theming**：Color only through semantic tokens: six presets plus base × theme color. Switching themes never touches product code.
- **Components by category**：Nine galleries: basic controls, forms, data display, feedback, navigation, charts, icons, theming and settings.
- **Three layout modes**：Sidebar, top + sidebar, and top-only navigation; sidebar width, radius, transitions and header action order are adjustable.
- **Charts with no dependency**：Line, column, donut, mini bars, bar list, heatmap, radar, funnel and gantt are hand-drawn SVG that follow semantic colors and dark mode.
- **Menus and permissions**：Menus can come from the backend: nesting, external links with an open mode, permission filtering; route guards fall back to 403 and buttons hide or disable through Can.
- **Bilingual and accessible**：One language entry point with type-enforced parity; keyboard reachable, managed focus, high contrast, color-weak and reduced motion.
- **Standard pages**：Dashboard, list, detail, settings, notification centre, sign-in/register/forgot-password — page parts are shared.
- **Command palette**：⌘K searches menus and the content already rendered on the current page, with pinyin, path and full keyboard support.
- **Docs site and AI friendly**：A VitePress docs site (with dead-link checks) plus one-command pnpm check ; AGENTS.md and decisions live with the code.

## 组件索引

- Basic controls：button / input / tag / progress
- Forms &amp; pickers：combobox / cascader / multi-select / upload
- Data display：table / tree / tree table / pager
- Feedback &amp; overlays：dialog / sheet / toast / states
- Navigation：breadcrumb / tabs / steps
- Metrics &amp; charts：line / radar / funnel / gantt
- Icons：full lucide set, click to copy
- Theme &amp; settings：palette / notifications / a11y

## 快速开始

1. Copy the directory into your product repo and rename package.json .
2. Swap the menu in src/app/navigation.ts , or wire the backend menu API.
3. Swap identity : the session and permission codes in src/app/session.ts .
4. Wire APIs : replace pages/sample-data.ts ; keep Loading / Empty / Error.
5. Swap copy and brand : src/lib/i18n.ts and public/brand/ .

```bash
pnpm add @runlume/admin-ui

# Or run the complete template
pnpm install
pnpm dev        # app on http://localhost:3200
pnpm docs:dev   # docs on http://localhost:3210
pnpm check      # format + types + lint + tests + build
```

## 相关入口

- 文档站：https://adoc.runlume.app
- 在线演示：https://ago.runlume.app
- 源码（Apache-2.0）：https://github.com/runlume/admin-design

