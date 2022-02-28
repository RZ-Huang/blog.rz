---
title: Instruction
description: This is a test post
date: 2022-02-27
tags:
  - test
layout: layouts/post.njk
draft: false
---

測試測試，麥克風測試，第一篇文章測試。

安安，大家好，我是 RZ，這裡是我新的 blog。

之前使用 Hexo 建立的 blog 被我玩壞了（慘況[在這](https://rz-huang.github.io/)），由於使用到的 Hexo theme 需要比較舊的 node.js 版本 build 完的靜態檔案才不會損毀（檔案產生不完全），覺得麻煩之下乾脆不如重開一個客製化程度比較高的 blog。

於是在各大版搜尋有沒有好用的部落格文章架構和文件轉譯 library。找著找著就看到有兩位大神（[Jason](https://jason-memo.dev/)、[Huli](https://blog.huli.tw/2021/08/22/eleventy-over-hexo/)）有在使用 11ty，同時也找到 google 做的效能優化版本，因此就直接先套用上他們的 template 省事與效能一兼二顧啦！目前的版面我只有稍微修改顏色和一些小樣式，還沒有完全摸透整個架構，主要是 `.njk` 的模板語法之前都沒碰過所以還很陌生。

而網域目前先用 Pages 預設的網域（沒加薪又通膨只好縮衣節食(Ｏ)），Pages 是 Cloudflare 公司旗下的某一個產品（以下除非特別提，否則出現「Pages」皆指此公司的產品），其實可以把它看作是類似 Github 的 Pages，至於為什麼我不直接用 Github 的 Pages，因為 Pages 裡面的功能還能跟 Cloudflare 其他產品做應用，比如寫一些無伺服器 function（他們家的 Worker 產品）、儲存資料（使用 Durable Objects）、放 image 或 video 在上面（不過要錢），同時架在 Cloudflare 服務上的網站也會提升 User 網站讀取速度，確保網站安全性也是他們的主力，還有就是上站新版本可以先用 preview 的網址（亂數網址）來看，沒問題再 deploy 到主線去。另外我想跟它們的產品混熟一點，免費方案的額度對於貧窮的開發者很便利，所以現在就是把這個 blog deploy 到 Pages 啦（雖然可能某些 Cloudflare 的產品 blog 應該用不到？）。

不過雖然我沒直接使用 Github 的 Pages 功能，但 deploy 到 Pages 的流程會需要經由 Github 之手來做 intergration。
簡單來說就是整個專案的 source code 還是放在 Github 上，只要在本地 `git push` 上去到 Github repo，Pages 那邊會偵測到：「哦，你 commit 了新的 log，那我就開始自動幫你 CI/CD 囉。」
沒錯，Pages 會幫你 CI/CD，而且內建可以選擇你要用什麼 framework deploy，讓我很意外的是 11ty 也是其中一個選項，太神啦，所以 CI/CD 的設定我沒寫半行，只有跟 Pages 說我要用 `npm run build` 作為 build 的指令這樣而已。整個過程不需要花 5 分鐘就 deploy 上去了。

之後預計優先新增/修改的功能應該會有以下這些：

- Archive 頁面
- Tags 頁面
- 首頁文章分頁
- 文章內容底下有前一篇/下一篇連結
- primary color 還在思考要不要再改
- dark mode

總之大概是這樣啦，至於為什麼要把 blog 取作 Boundarylesstacks，只是因為看到有些人會幫 blog 取個名字，同時覺得 blog 可以有個象徵性的精神，於是就把 Boundaryless 和 stacks 兩個單字合在一起，把這裡當作是沒有限制性任何 stack 都可以作為內容，把任何事情都當作 stack 的概念，同時也有想要慢慢累積各式各樣的知識的這種感覺，也呼應之前 Hexo blog 那邊的標語：「積少成多; 積少化痰。」（後面那句只是硬湊沒特別意思）。
