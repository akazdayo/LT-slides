---
marp: true
theme: gaia

---

# 完全に再現可能なインフラを構築してみよう

---

## 従来のインフラ構築手順

1. ベンダーのWebサイトにアクセス
2. 新しいコンテナ/VMを立てる
3. SSHでごちゃごちゃ
4. なんか動いたっ！

## 問題点

- 変更点をチームで共有しにくい
- Gitでバージョン管理ができない
- **ミスをしたときに本番環境がストップする可能性がある**


---

## じゃあどうする？
1. TerraformでベンダーのWeb操作を自動化
2. NixOSを使ってOSの操作に再現性を持たせる

![Image](https://brand.nixos.org/logos/nixos-logo-default-gradient-black-regular-horizontal-recommended.svg)

---

## これをやる素敵さ
- GUIとか言う諸悪の根源を触る必要がない
  - Webサイトは人間用のインターフェイスなのでわかりにくい
- shellを触る必要がない
- **ビルドエラーが発生する**
  - インフラをビルドできるので、悪い操作をしたときに自動的にビルドエラーが発生する

---

## 簡単に試してみよう

---

![bg opacity](https://picsum.photos/800/600?image=53)
## 7. Columns

<div class="columns">
<div>

## Left

- 1
- 2

</div>
<div>

## Right

- 3
- 4

</div>
</div>

---

## 8. Icons

<i class="fa-brands fa-twitter"></i> Twitter: 
<i class="fa-brands fa-mastodon"></i> Mastodon: 
<i class="fa-brands fa-linkedin"></i> LinkedIn: 
<i class="fa fa-window-maximize"></i> Blog: 
<i class="fa-brands fa-github"></i> GitHub: 

---

# 9. <!--fit--> Large Text

---

<!-- Needed for mermaid, can be anywhere in file except frontmatter -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

# 10. Mermaid

<div class="mermaid">
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
</div>
