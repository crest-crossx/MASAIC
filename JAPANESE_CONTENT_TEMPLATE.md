# Japanese Content Template

Use this file as a small reference when adding Japanese content to MASAIC pages.

## Common Labels

| English | Japanese |
| --- | --- |
| Home | ホーム |
| About | 概要 |
| Teams | チーム |
| Members | メンバー |
| Publications | 研究論文 |
| News | ニュース |
| Schedule | スケジュール |
| Seminar | セミナー |
| Collaboration | 共同研究 |
| Sponsors | スポンサー |
| Contact Us | お問い合わせ |
| Learn More | 詳しく見る |
| Read More | 続きを読む |

## Research Terms

| English | Japanese |
| --- | --- |
| Robotics | ロボティクス |
| Control | 制御 |
| AI Integration | AI統合 |
| Large Language Model | 大規模言語モデル |
| Neuromorphic Sensing | ニューロモルフィックセンシング |
| VR/AR | VR/AR |
| Imitation Learning | 模倣学習 |
| Human-Robot Interaction | 人間ロボットインタラクション |
| Multi-Agent System | マルチエージェントシステム |
| Autonomous System | 自律システム |
| Machine Learning | 機械学習 |
| Deep Learning | 深層学習 |

## Section Pattern

```html
<div data-lang-content="en">
    <h2>Research Focus</h2>
    <p>English content goes here.</p>
</div>

<div data-lang-content="ja" style="display: none;">
    <h2>研究重点</h2>
    <p>Japanese content goes here.</p>
</div>
```

## Checklist

- Add both English and Japanese blocks for long sections.
- Use `data-i18n` for short repeated labels.
- Keep links, email addresses, file paths, and IDs unchanged.
- Test language switching on desktop and mobile.
- Confirm Japanese text does not overflow buttons, cards, or navigation items.
