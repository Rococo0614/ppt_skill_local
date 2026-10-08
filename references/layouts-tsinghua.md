# 清华大学风格 · 版式说明（Tsinghua Layouts）

> **风格 C · 清华风 = Swiss 版式体系 + 清华紫锚点色**。
> 本文件是 `layouts-swiss.md` 的引用转发:所有正文版式 **S01-S22 与 Swiss 风完全一致**,版式锁、图片规则、字号分档、校验器全部复用,**唯一变化是锚点色换成清华紫**。

---

## 快速使用

1. 模板用 `assets/template-tsinghua.html`(从 `template-swiss.html` 派生,类名、JS、演讲者模式逐字节一致)
2. 版式骨架直接读 `references/layouts-swiss.md` 粘贴,**data-layout 仍写 `S01-S22`**
3. 版式锁仍由 `references/swiss-layout-lock.md` 约束,校验仍跑:

```bash
node <SKILL_ROOT>/scripts/validate-swiss-deck.mjs path/to/index.html
```

4. 主题色从 `references/themes-tsinghua.md` 4 套紫色里选一套,替换 `:root` 主题色变量即可

---

## 与 Swiss 风的差异清单(仅 4 处,其余全同)

| 项目 | Swiss 风 | 清华风 |
|---|---|---|
| 模板 | `assets/template-swiss.html` | `assets/template-tsinghua.html` |
| 锚点色 | IKB 克莱因蓝 `#002FA7` | 清华紫 `#660874`(3 个变体+1 紫灰) |
| 暗底高亮 | `--accent-bright:#5B7BFF` | `--accent-bright:#A55FCC` |
| 低功耗事件名 | `swiss-low-power-change` | `tsinghua-low-power-change` |

`.swiss-*` 类名（`.swiss-img-split` / `.swiss-keyline` / `.swiss-lined` 等）**在清华模板里保留原名不动**——它们是版式契约的一部分,改名会导致 layouts-swiss.md 骨架全部失效。

---

## 清华风专属文案建议

- chrome 元数据可用 `Tsinghua` / `Academic` / `THU` 强化语义
- 校训「自强不息 厚德载物」可作为封面副标或收束金句(文字即可,不要贴校徽图)
- 封面 `.slide.accent` 满屏清华紫 + ASCII 呼吸场,收尾右半第 03 条 takeaway 用 `var(--accent)` 首尾色彩闭环——与 Swiss 封面/封底结构完全相同

## 适用场景

学术汇报、科研答辩、论文分享、课程讲座、毕业/校庆主题、技术教育内容。
美学锚点:清华校徽紫 × 瑞士国际主义网格,像"把 Massimo Vignelli 的网格贴上了校色"。

## 版式多样性硬规则(沿用 Swiss)

- 7-8 页 deck 至少 6 个不同 S 编号;10 页以上至少 8 个
- 不允许连续 3 页同一主体结构;单张大图用 S22,多图用 S15/S16 网格改造
- 交付前跑 `validate-swiss-deck.mjs`(对清华模板同样有效,data-layout 仍校验 S01-S22)
