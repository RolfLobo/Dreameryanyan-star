# 单图 Prompt 模板 · 8 段式

**所有小星妍风格图都用这个 8 段结构写英文 prompt。** 顺序不能乱——是模型解析的层级。

## 完整模板

```text
Generate one standalone [ASPECT RATIO] editorial illustration in the tradition of Tom Gauld and Christoph Niemann — one bold concept, massive white space, unified hand-drawn parallel-hatching pen-stroke language.

Visual DNA:
[PAPER COLOR + HEX]. Around [X]% empty paper (mostly [WHERE]). Confident hand-drawn warm-ink line work. Structural hatching only where volume/shadow makes sense. NO decorative elements, NO sparkles, NO patterns, NO shine.

Recurring IP character (Xingyan / 小星妍):
A small hand-drawn honey-yellow five-pointed star with gently rounded but clearly star-shaped points, drawn with a slight wobble and a subtle tilt to one side — she is never stiffly upright. Warm-black wobbly hand-drawn outline (#1a1614). Two tiny black dot eyes, slightly asymmetric, curious. A tiny mouth mark is allowed — a single short curved line, either a small "o" of curiosity or a barely-there upward arc — never a big cartoon grin. Thin black legs, drawn in a lively [POSE VERB: mid-hop / mid-stride / braced stance / tiptoe / whoa gesture] — never planted stiffly like standing at attention. One thin black arm from a side point [ACTION: holding a pen / reaching upward / gesturing outward] with visible energy. 6-10 short parallel diagonal hatching strokes on her lower-right side for volume.

Dreamer signature: directly above her head, tucked close to the crown, a very SMALL handwritten "Dreamer" arcs gently in warm honey ink. Size ~1/9 her body height. Tight small curve, NOT a rainbow.

Status glyph (above the Dreamer arc): a tiny hand-drawn [GLYPH NAME from status-glyphs.md] in honey-yellow outline only (no fill), [SHAPE DESCRIPTION], floating just above the Dreamer arc — her "[STATE]" state. Size ~1/5 her body height. NO decorations, NO sparkles, NO fill.

Signature bottom-right: tiny handwritten "[妍 ✦ or Xingyan ✦]" in warm honey ink.

Single visual concept:
[ONE-SENTENCE lock-in of what this image is saying. Include the reversal / contrast hook.]

Composition ([RATIO] vertical/horizontal):
- [Upper / Left] X% of canvas: [what's here]
- [Middle band]: [小星妍 + her exact pose + her hatching]
- [Lower / Right] Y% of canvas: [what's here + tiny secondary element]

[LANGUAGE] handwritten labels ([only N, small]):
- [Position]: [Chinese or English text] (small, [color])
- [Position]: [Chinese or English text] (small, [color])

Hatching language (unified):
Warm-black short parallel diagonal strokes, same angle everywhere, three places only: (1) [where + count], (2) [where + count], (3) [where + count]. NO hatching in [where].

Color use (strict):
- Paper: [warm cream #fbf8f0 / pure white #ffffff].
- Honey-yellow ONLY on Xingyan's body, the tiny "Dreamer" arc, and the tiny [glyph name] status glyph outline above her head.
- Warm-black ink for: [enumerate everything black].
- [Red / Blue / Orange] ONLY for [what].
- No other colors.

Anti-slop constraints:
- [PAPER constraint: NO cream/texture OR NO tint depending on paper choice]
- [IP-shape constraint: specific to this image]
- [SAMENESS constraint: e.g., two figures must be same height]
- [MISC anti-decoration: NO gradient, NO plastic shine, NO decorative sparkles, NO hearts, NO extra stars]
- [LANGUAGE constraint: all text in Chinese/English only]
- Dreamer text tiny, hugs her crown.
- At least X% of the canvas is empty [color] paper.
```

## 每段的作用

| 段 | 作用 | 常见坑 |
|---|---|---|
| 1. Opener | 定框架：编辑插画 + 对标名 + 尺寸 + 手绘语言 | 别忘对标名 Tom Gauld × Niemann |
| 2. Visual DNA | 定纸底 + 留白率 + 无装饰基调 | 留白率必须写数字（模型对模糊描述不敏感） |
| 3. Recurring IP character | 定小星妍完整规格 | 姿态动词必须具体（不能只写"lively"） |
| 4. Dreamer signature | 定静态签名 | 一定要写"tight small curve, NOT a rainbow" |
| 5. Status glyph | 定动态签名 | 明确写 "outline only, no fill" |
| 6. Bottom-right signature | 定右下角签名 | 别忘 |
| 7. Single visual concept | 一句话锁定这张图讲什么 | 越具体越好，包含反差抓手 |
| 8. Composition | 精确分区 + 小星妍在哪 + 每个 % 装什么 | 用 %，别用"上面 / 下面" |
| 9. Labels | 中文/英文小标签 | 最多 2 个，颜色对偶 |
| 10. Hatching | 三处排线的精确位置 | 一定要 "three places only" |
| 11. Color use | 严格颜色系统 | 一定要 "ONLY" 关键词 |
| 12. Anti-slop | 反 slop 底线 | 越具体越好，直接写"NO X" |

## Prompt 大小规模

- 一张单图 prompt 一般 **400-700 词**
- 少于 300 词的 prompt 模型自由发挥空间过大，容易崩
- 超过 900 词的 prompt 模型开始漏读，反而不稳定

## 用户交付格式

给用户时：
1. **一段中文说明**：这张图放在哪一段 / 核心讲什么 / 为什么这么画
2. **一个代码块**（```text ... ```）**装完整英文 prompt**
3. 用户可以复制 prompt 直接喂给图像模型

## 完整实例

见 `examples/prompts-6-vertical-final.md` 里的 6 张。**参考它们的结构和 anti-slop 密度，不要复刻它们的构图和物件**。
