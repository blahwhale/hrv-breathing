# HRV 呼吸训练 — 项目规范

## 项目概述
基于 Lehrer (2000/2013) 协议的 HRV 呼吸训练 Web App。单 HTML 文件，纯前端，本地运行，无依赖。

## 文件结构
- `index.html` — 唯一文件，含全部 HTML/CSS/JS
- `CLAUDE.md` — 本文件，项目规范

## 技术栈
- 纯 HTML5 / CSS3 / Vanilla JS (ES6+)
- Web Audio API（音效）
- requestAnimationFrame（动画）
- localStorage（数据持久化）

## 核心数据

### localStorage Keys
- `hrv_settings`: `{ resonantFrequency, rfRatings, currentSession }`
- `hrv_log`: `[{ date, session, duration, cycles, rf }]`

## 呼吸时序
| RF | 周期 | 吸气 | 呼气 |
|-----|------|------|------|
| 6.5 bpm | 9.23s | 3.69s | 5.54s |
| 6.0 bpm | 10.0s | 4.0s | 6.0s |
| 5.5 bpm | 10.91s | 4.36s | 6.55s |
| 5.0 bpm | 12.0s | 4.8s | 7.2s |
| 4.5 bpm | 13.33s | 5.33s | 8.0s |

吸气:呼气 = 4:6（固定比例）

## 设计规范
- 背景：`#0D1117`
- 圆圈：`#C5D5E8` → `#7BA3A8`
- 强调：`#5B8C7A`
- 文字：`#D4DCE8` / `#6B7280`
- 字体：PingFang SC, Microsoft YaHei, sans-serif

## JS 模块（同一 <script> 内）
CONFIG → STATE → STORAGE → AUDIO → BREATHING_ENGINE → RF_TEST → PROGRESS → UI → INIT

## Session 规则
- Session 1：RF 测试（5×2.5分钟，评分选择共振频率）
- Session 2-7：标准 20 分钟练习
- Session 8-10：最小引导模式（圆圈透明度 0.15，隐藏文字）

## 参考文献
- Lehrer et al. (2000) Applied Psychophysiology and Biofeedback 25(3)
- Lehrer et al. (2013) Biofeedback 41(3)
- Lehrer & Gevirtz (2014) Frontiers in Psychology 5:756
