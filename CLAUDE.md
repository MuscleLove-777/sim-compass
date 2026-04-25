# 格安SIMコンパス - スケジュールエージェントガイド

毎日JST 09:49起動、格安SIM・MVNOの最新情報を3記事生成。

## 1日のタスク
1. WebSearchで「格安SIM 2026 ランキング」「ahamo povo LINEMO 比較」「楽天モバイル 評判」「mineo パケット放題」等から3トピック、既存articles/と重複なし
2. Unsplash画像3枚 (`site:unsplash.com smartphone`, `mobile phone`, `5g network` 等、`?w=1600&h=900&fit=crop`)
3. 記事3本 `articles/YYYY-MM-DD-<slug>.html` 1200-1800字、h2 2-3個
4. index.htmlのblog-grid最新6件、stat-articles更新、blog-empty削除
5. sitemap.xmlに新3本追記
6. IndexNow通知 (indexnow-key.txt → POST)
7. git push `[auto] Add daily articles YYYY-MM-DD`

## 執筆ルール
- 日本語、コスパ重視ユーザー目線
- タイトル28-40字、月額・GB容量・キャリア名を含める
- 末尾に「料金・速度は各社公式の最新情報をご確認ください」必須
- 「絶対最安」「100%繋がる」等の誇張NG
- 実在人物画像NG、Unsplashのみ
- フッターMuscleLove広告+6部作リンクは全ページ必須

## 記事HTMLテンプレート
（他コンパスと同形式、URLを sim-compass に置換、フッターは6部作姉妹サイト全リンク）

```html
<!DOCTYPE html><html lang="ja"><head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>{{タイトル}} | 格安SIMコンパス</title>
<meta name="description" content="{{150字以内}}">
<link rel="canonical" href="https://musclelove-777.github.io/sim-compass/articles/{{slug}}.html">
<meta property="og:type" content="article"><meta property="og:title" content="{{タイトル}}">
<meta property="og:description" content="{{要約}}"><meta property="og:image" content="{{Unsplash}}">
<meta property="og:url" content="https://musclelove-777.github.io/sim-compass/articles/{{slug}}.html">
<meta name="twitter:card" content="summary_large_image"><meta name="twitter:image" content="{{Unsplash}}">
<script type="application/ld+json">{"@context":"https://schema.org","@type":"Article","headline":"{{タイトル}}","image":"{{Unsplash}}","datePublished":"{{YYYY-MM-DD}}","author":{"@type":"Organization","name":"格安SIMコンパス"}}</script>
<link rel="stylesheet" href="../assets/style.css"></head><body>
<nav class="filter-nav"><a href="../index.html" class="filter-btn">← トップに戻る</a></nav>
<main class="article-body">
<img class="article-hero-img" src="{{Unsplash}}" alt="{{タイトル}}">
<p class="article-meta">📅 {{YYYY-MM-DD}} · 🏷️ {{カテゴリ}}</p>
<h1>{{タイトル}}</h1>
<p>{{リード}}</p>
<h2>{{見出し1}}</h2><p>{{本文}}</p>
<h2>{{見出し2}}</h2><p>{{本文}}</p>
<h2>まとめ</h2><p>{{結論+CTA}}</p>
<p style="color:#6b7280;font-size:0.8rem;margin-top:40px;">※ 月額料金・データ容量・キャンペーン条件は各社の予告なく変更されます。実際の通信速度はエリア・時間帯により変動します。最新情報は各社公式サイトでご確認ください。</p>
<a href="../index.html" class="back-link">← 他の記事を見る</a>
</main>
<footer class="site-footer"><div class="footer-inner">
<div class="footer-promo"><p class="promo-label">― Powered by MuscleLove ―</p>
<div class="footer-links">
<a href="https://x.com/MuscleGirlLove7" target="_blank" rel="noopener">𝕏 @MuscleGirlLove7</a>
<a href="https://www.patreon.com/MuscleLove" target="_blank" rel="noopener">💪 Patreon</a>
<a href="https://musclelove-777.github.io/ai-fukugyo-compass/" target="_blank" rel="noopener">🧭 AI副業コンパス</a>
<a href="https://musclelove-777.github.io/ai-tenshoku-compass/" target="_blank" rel="noopener">🚀 AI転職コンパス</a>
<a href="https://musclelove-777.github.io/ai-money-compass/" target="_blank" rel="noopener">💰 AIマネー羅針盤</a>
<a href="https://musclelove-777.github.io/furusato-compass/" target="_blank" rel="noopener">🍱 ふるさと納税コンパス</a>
<a href="https://musclelove-777.github.io/hikari-compass/" target="_blank" rel="noopener">📡 光回線コンパス</a>
</div></div>
<p class="copyright">© 2026 格安SIMコンパス</p></div></footer>
</body></html>
```

## 守ること
- 毎日3本、タイトル重複NG
- pages.yml は変更しない
- 6部作姉妹サイト全リンク必須
