---
theme: apple-basic
drawings:
  persist: false
mdc: true
layout: intro
transition: null
---

# 自己紹介

---

# 自己紹介

<div class="flex justify-center mt-0 pt-0">
  <div class="pt-6 pb-24 px-24 text-center flex flex-col items-center">
    <img src="https://avatars.githubusercontent.com/u/82073147?v=4" class="rounded-full w-48 h-48 border-1 border-gray-200 shadow-md mx-auto" />
    <h2 class="text-gray-500 font-bold mt-4">@akazdayo</h2>
    <h1 class="mt-2">あかず</h1>
  </div>
  <div class="pt-6 pb-24 px-24 text-left overflow-hidden">
    <h2>趣味</h2>
    <div class="text-left">
      <ul>
        <li>プログラミング
          <ul>
            <li>Typescript</li>
            <li>Nix</li>
            <li>Python</li>
            <li>その他</li>
          </ul>
        </li>
        <li>技術的なこと全般</li>
        <li>ゲーム
          <ul>
            <li>osu!</li>
            <li>VRChat</li>
            <li>etc...</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</div>

---
layout: center
---

# みなさん、NixOSって知ってますか？

---
layout: center
---

## WindowsやMacと同じ「OS」の一種です

Linux系のオペレーティングシステム

---

## OSって？

- **オペレーティングシステム（OS）**
  - パソコンを動かすための基本ソフト
  - Windows、macOS、Linuxなど

- **NixOS**
  - Linuxの一種
  - 「再現可能」で「宣言的」なのが特徴

---
layout: two-cols
---

## Windows/macOSでの作業

新しいPCを買ったとき...

1. アプリを1つずつインストール
2. 設定を手動で変更
3. 壁紙やテーマを設定
4. **前のPCと全く同じにするのは困難**

<br>

💻 「あれ、前のPCでは何のソフト入れてたっけ...？」

::right::

## NixOSでの作業

新しいPCを買ったとき...

1. **設定ファイル1つをコピー**
2. コマンド1つ実行
3. **完了！前のPCと全く同じ環境**

<br>

✨ 「設定ファイルがあれば、いつでも同じ環境が作れる！」

---
layout: fact
---

<h2 class="text-center">
  設定ファイル1つで
  <br>
  環境が完全に再現できる
  <br>
  それがNixOS
</h2>

---
layout: two-cols
---

## 一般的なOS（Windows/macOS）

- **アプリのインストール**
  - クリックしてインストーラー実行
  - 設定は手動で変更
- **問題点**
  - 「何をインストールしたか」忘れる
  - 設定を元に戻せない
  - 別のPCで同じ環境を作るのが大変

::right::

## NixOS

- **アプリのインストール**
  - 設定ファイルに書くだけ
  - 設定も全てファイルで管理
- **利点**
  - 何をインストールしたか記録される
  - いつでも前の状態に戻せる
  - 別のPCでも同じ環境を簡単に構築

---
layout: two-cols
---

## NixOSの特徴

- **宣言的な設定**
  - すべての設定が1つのファイルで管理
- **再現可能**
  - 同じ設定から同じ環境が構築される
- **ロールバック可能**
  - いつでも前の状態に戻せる
- **安全なアップグレード**
  - 壊れても前の世代に戻れる

::right::

## 従来のLinuxとの違い

- **従来**: 手作業での設定変更
  - 再現が困難
  - 環境が徐々に汚れる
- **NixOS**: 設定ファイルで宣言
  - 完全に再現可能
  - クリーンな環境を維持

---

## 設定例: configuration.nix

```nix
{ config, pkgs, ... }:

{
  # システム設定
  networking.hostName = "my-nixos";

  # パッケージのインストール
  environment.systemPackages = with pkgs; [
    vim
    git
    firefox
  ];

  # サービスの有効化
  services.openssh.enable = true;

  # ユーザー設定
  users.users.akazdayo = {
    isNormalUser = true;
    extraGroups = [ "wheel" ];
  };
}
```

---
layout: two-cols
---

## NixOSの良いところ

- 環境の完全な再現性
- 複数バージョンの共存が可能
- 安全な実験ができる
  - 失敗しても簡単にロールバック
- dotfilesとの相性が良い
  - Gitでバージョン管理できる

::right::

## NixOSの大変なところ

- 学習曲線が急
  - Nix言語を学ぶ必要がある
- 情報が少ない
  - 日本語の情報は特に少ない
- 既存の知識が使えないことも
  - FHS準拠ではない
- ビルド時間が長いことがある

---
layout: center
---

## それでもNixOSを使う理由

**一度設定すれば、どこでも同じ環境が手に入る**

新しいマシンでも、クラウドでも、コンテナでも
<br>
設定ファイルを適用するだけで同じ環境が完成

---
layout: center
---

ご清聴ありがとうございました！
