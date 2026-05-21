# Japanese Content Snippets

This file provides clean examples for adding Japanese content to MASAIC pages.

## Page Header Pattern

```html
<section class="team-header">
    <div class="container">
        <div data-lang-content="en">
            <h1>News & Updates</h1>
            <p>Latest news, achievements, and announcements from MASAIC</p>
        </div>
        <div data-lang-content="ja" style="display: none;">
            <h1>ニュース・最新情報</h1>
            <p>MASAICの最新ニュース、成果、お知らせ</p>
        </div>
    </div>
</section>
```

## Content Block Pattern

```html
<div data-lang-content="en">
    <h2>Research Publications</h2>
    <p>Research papers and publications from the MASAIC project.</p>
</div>

<div data-lang-content="ja" style="display: none;">
    <h2>研究論文</h2>
    <p>MASAICプロジェクトの研究論文と出版物。</p>
</div>
```

## Common Terms

```text
Home: ホーム
About: 概要
Teams: チーム
Members: メンバー
Publications: 研究論文
News: ニュース
Schedule: スケジュール
Seminar: セミナー
Collaboration: 共同研究
Sponsors: スポンサー
Contact Us: お問い合わせ
Read more: 続きを読む
Learn More: 詳しく見る
```

## Recommended Workflow

1. Add the English content first.
2. Add a matching Japanese block with `data-lang-content="ja"`.
3. Keep both blocks in the same parent container.
4. Test the language switcher on desktop and mobile.
5. Check that text does not overflow cards, buttons, or navigation items.
