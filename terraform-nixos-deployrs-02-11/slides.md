---
theme: apple-basic
drawings:
  persist: false
mdc: true
layout: intro
transition: null
---

# Terraform × NixOS × deploy-rs
## インフラ管理が楽しくなる3点セット

---
layout: center
---

## Terraformの魅力

- クラウド構成をコードで管理できる
- planで「何が変わるか」を事前に確認できる
- チームで同じ状態を再現しやすい

<p class="mt-6 text-gray-500">「作って終わり」ではなく、継続的に安全に運用できる。</p>

---
layout: center
---

## NixOSの魅力

- OS設定そのものを宣言的に書ける
- 再現性が高く、環境差分が減る
- ロールバックが簡単で失敗に強い

<p class="mt-6 text-gray-500">サーバー設定が「職人芸」から「共有可能なコード」へ。</p>

---
layout: center
---

## deploy-rsの魅力

- NixOSマシンへのデプロイをシンプルに自動化
- 複数ホストへ安全に段階適用できる
- flakeと組み合わせると運用フローが統一される

<p class="mt-6 text-gray-500">"どの手順で反映したか" をコードとして残せる。</p>

---
layout: center
---

## まとめ

- **Terraform**: クラウド構成管理
- **NixOS**: サーバー設定管理
- **deploy-rs**: デプロイ管理

<p class="text-2xl mt-8 font-bold">3つを組み合わせると、インフラ運用がかなり快適になる！</p>
