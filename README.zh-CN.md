# Materializr 中文版

基于 [materializr-cad/materializr](https://github.com/materializr-cad/materializr) 的简体中文版本：在官方多语言框架内新增 **简体中文** 界面语言，并内置中文字体。

## 改动内容

- **简体中文界面**：全量翻译 1438 条 UI 字符串（工具/菜单/设置/提示/快捷键等），在设置中选择「简体中文」即可实时切换，无需重启。
- **中文字体**：内置 Noto Sans SC（SIL OFL 1.1），作为 UI 字体的 CJK 回退合并，中文、以及项目名/路径中的汉字都能正常显示。
- **中文文字雕刻**：草图文字工具新增「中文 (Noto Sans SC)」字体，可直接雕刻汉字。
- 翻译源在 `tools/i18n_zh.py`（英文串即键），改完跑 `python tools/i18n_catalogue.py` 重新生成 `src/i18n_catalogue.h`。

## 构建

与上游完全一致，见 [BUILD.md](BUILD.md) 与 [docs/building.md](docs/building.md)。Windows 用 vcpkg + CMake（`vcpkg.json` 已固定 OpenCASCADE 7.9.3），Linux/macOS/Android/iPad 按上游文档。

## 与上游同步

上游更新后拉取合并，若英文串有增删：新串会自动回退英文显示，把新键补进 `tools/i18n_zh.py` 后重新生成即可，不会有红字或崩溃。

## 许可

代码遵循上游 GPLv3；新增字体 Noto Sans SC 遵循 SIL OFL 1.1（见 `assets/fonts/FONT-CREDITS.md`）。
