# DreamerStar Editorial Illustration Skill

[English](README.md) | [中文](README_CN.md)

A Claude / Copilot skill for creating editorial illustrations in the **DreamerStar (小星妍)** visual language.

> A honey-yellow star character meets minimalist conceptual illustration inspired by editorial cartooning.
> One image = one idea + generous negative space + three structural hatching areas + a visual contrast hook.

## What It Is

DreamerStar (小星妍) is a slightly tilted, honey-yellow five-pointed star. She has a small curved "Dreamer" wordmark close above her head, hand-drawn hatching on one lower side, and a contextual status glyph such as a light bulb, `?`, crown, cloud, lightning bolt, spark, or speech bubble. She must take part in the image's central action and never appear as decoration.

**Best for:** editorial illustrations for Chinese articles, Xiaohongshu posts, presentations, Notion documents, and social media covers. The primary format is 3:4 portrait, with 4:3 and 1:1 also supported.

**Not intended for:** portrait-led covers, polished 3D commercial illustration, or presentation-style infographics and architecture diagrams.

## Project Structure

```text
dreamerstar/
├── SKILL.md                        Main entry: positioning and five-step workflow
├── references/
│   ├── style-dna.md                Visual DNA, color, negative space, and hatching
│   ├── xiaoxingyan-ip.md           Complete character specification and pose library
│   ├── status-glyphs.md            15 status glyphs across five families
│   ├── composition-patterns.md     Composition principles, contrast hooks, and formats
│   ├── prompt-template.md          Eight-part English prompt template
│   └── qa-checklist.md             Post-generation QA and anti-slop checklist
├── example/                        Nine finished images shown in the gallery below
└── examples/
    ├── ai-era-product-interview-v6.2.md   Seven v6.2 prompt examples
    ├── six-vertical-illustrations.md      Six earlier portrait examples
    ├── four-poses/                        Pose studies
    └── ip-manual/                         Character manual
```

## Usage

### Install as a Claude Code or Copilot skill

```bash
# Claude global skill
ln -s "$(pwd)" ~/.claude/skills/dreamerstar

# Or Copilot global skill
ln -s "$(pwd)" ~/.copilot/skills/dreamerstar
```

Then start a new conversation and say: `Use DreamerStar to illustrate this article` or `Generate a thinking pose with DreamerStar`.

### Use as a prompt library

You can also copy a prompt from [`examples/ai-era-product-interview-v6.2.md`](examples/ai-era-product-interview-v6.2.md) into an image model such as GPT Image, Nano Banana, or Midjourney.

## Examples

<table>
    <tr>
        <td><img src="example/71ceb6fd-f2c3-42c4-b419-3e87dc9a2bce.jpeg" width="240" height="320" alt="DreamerStar example 1"></td>
        <td><img src="example/Gemini_Generated_Image_7yx70x7yx70x7yx7.png" width="240" height="320" alt="DreamerStar example 2"></td>
        <td><img src="example/Gemini_Generated_Image_c2j3vhc2j3vhc2j3.png" width="240" height="320" alt="DreamerStar example 3"></td>
    </tr>
    <tr>
        <td><img src="example/Gemini_Generated_Image_r5nht8r5nht8r5nh.png" width="240" height="320" alt="DreamerStar example 4"></td>
        <td><img src="example/Screenshot%202026-07-18%20at%204.07.25%E2%80%AFPM.png" width="240" height="320" alt="DreamerStar example 5"></td>
        <td><img src="example/Gemini_Generated_Image_w368oyw368oyw368.png" width="240" height="320" alt="DreamerStar example 6"></td>
    </tr>
    <tr>
        <td><img src="example/be47bbf4-6d72-4e60-91fb-be46e41d7380.jpeg" width="240" height="320" alt="DreamerStar example 7"></td>
        <td><img src="example/c29d3e5a-ec58-48a1-a1b1-9c5dad9d6762.jpeg" width="240" height="320" alt="DreamerStar example 8"></td>
        <td><img src="example/e66317aa-5aff-4fed-a55a-6fa4eab4938e.jpeg" width="240" height="320" alt="DreamerStar example 9"></td>
    </tr>
</table>

## Core Principles

- **One image, one idea.** Do not turn an illustration into an infographic or architecture diagram.
- **55-65% negative space.** Empty space gives the concept room to breathe.
- **Three structural hatching areas** at a consistent angle. Hatching elsewhere becomes visual noise.
- **A clear contrast hook.** Top versus bottom, before versus after, definition versus optimization, or individual versus group should read in a second.
- **The status glyph is the second-read clue.** Choose the symbol that best answers: "What is she primarily thinking or feeling right now?"
- **She is always doing something.** Never pose her at attention or use her as decoration. A small jump is better than a static stance.

## License

MIT. See [LICENSE](LICENSE).

The DreamerStar character, status-glyph system, and composition language are open for learning and remixing. Please provide attribution when using them commercially.

## References and Acknowledgements

This project draws on Ian's open-source work in [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations), particularly its approach to extracting cognitive anchors from Chinese writing, building shot lists, and structuring editorial illustration workflows. Thank you to Ian for sharing the methodology.
