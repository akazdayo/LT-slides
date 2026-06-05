---
theme: apple-basic
drawings:
  persist: false
mdc: true
layout: intro
transition: null
---

# NixOSでプログラマにとって超快適なMinecraftサーバーを構築してみる

---

# 自己紹介

<div class="flex justify-center mt-0 pt-0">
  <div class="pt-6 pb-24 px-24 text-center flex flex-col items-center">
    <img src="https://cdn.nostrcheck.me/1beecee55f69ebc2890403606f28b5e8ebbab23d226730e12b4bf762d29d2162/0c485cbf8db44882b730926366e545d211145cf1fee8b19909fa192e0e6d0443.webp" class="rounded-full w-48 h-48 mx-auto" />
    <h2 class="text-gray-500 font-bold mt-4">@akazdayo</h2>
    <h1 class="mt-2">あかず</h1>
  </div>
  <div class="pt-6 pb-24 px-24 text-left overflow-hidden">
    <h2>未踏ジュニアでやってた</h2>
    <div class="text-left">
      <ul>
        <li>aikyoを作っていた</li>
        <li>マルチパーティAIエージェントの<br/>操作とかは話せそう</li>
      </ul>
    </div>
    <h2>趣味</h2>
    <div class="text-left">
      <ul>
        <li>技術
          <ul>
            <li>Nix</li>
            <li>Nostr</li>
          </ul>
        </li>
        <li>ゲーム
          <ul>
            <li>osu!</li>
            <li>VRChat</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</div>

---

## layout: two-cols

# Nixとかいうやつ

- Nix!=NixOS
-

::right::

<img src="https://brand.nixos.org/logos/nixos-logo-default-gradient-black-regular-vertical-recommended.svg"/>

---

# プログラマにやさしいらしい

例えばGitなら

```nix
  programs.git = {
    enable = true;
    lfs.enable = true;
    settings = {
      user = {
        name = "akazdayo";
        email = "82073147+akazdayo@users.noreply.github.com";
      }
      init = {
        defaultBranch = "main";
      };
    };
  };
```

---

# マイクラサーバー管理者ってめんどくさい...

例えば...

- MODいれてー
- サーバー落ちたんだけど
- 俺のことホワイトリスト, OP追加して
- プロキシの設定して

---

# いやいや、そんなのお前がやれよ

ができます

---
