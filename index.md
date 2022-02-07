---
marp: true
theme: gaia
header: 唐澤克幸(K021C1260)
backgroundColor: lavender
paginate: true
---

# アラートループ事件
Webサイトの利用者に対する攻撃の事例
Webサイトの改竄やWebサイトのサービスに対する攻撃
    K021C1260:唐澤克幸

**Github Repository**
https://github.com/Katsuyuki-Karasawa/1st-marp-ghpages
Source is No License

---

# 目次

1. 概要
2. プログラム概要
3. 反響
4. みんなで逮捕されようプロジェクト
5. 結論
6. 文献およびソース
7. 最後に

---
# はじめに
このレポートはMarpによって作成されており、自分のポートフォリオ、およびSpeaker Deckにも同様のものがポストされています
Github Pagesによってホスティングされているため、オープンソースですが、No Licenseです。

これは2019年3月に発生した、無限アラート事件、兵庫県警ブラクラ摘発事件と呼ばれる事件について取り上げています

---

# 概要

**2019年3月**
兵庫県警は電子掲示板に**不正プログラムへのリンクを書き込んだ**不正指令電磁的記録供用未遂の疑いで逮捕 **(あくまで設置者は別である)**:thinking:

女子中学生を家宅捜索のち触法少年として補導
男性2人を家宅捜索・書類送検した

**3/26**
2018年に別の男子中学生と男子大学生も摘発されていたことが判明した

---
### これに対し
 * **3月25日**
 日本ハッカー協会が男性2人の弁護士・裁判費用の援助のための寄付の受付を開始

 * **翌26日**
 同団体は計553人の支援者から約700万円の寄付が集まったことを公表し、寄付の受付を終了することを発表:raised_hands:

 * **同年5月29日**
 男性2人の起訴猶予を理由とした不起訴処分:+1:

---

検察側は「ウイルス罪を成立させる要件の1つ『反意図性』に抵触する。そのため男性の行為はウイルス罪に該当する」との認識

そのため、不正指令電磁的記録供用罪に該当するという主張を変えなかった

弁護を担当した弁護士2名が、起訴猶予処分に対し『犯罪にあたると考えるが今回だけは起訴しないでおいた』という姿勢でお茶を濁した」「嫌疑なしとすべきだった」と、検察を批判する声明を発表

[**アラートループ事件の被疑者２名に対する起訴猶予処分を受けて**](https://www.yokohama-park-law.com/news/20190529.html)

---
# プログラム概要

```js
for ( ; ; ) {
window.alert("　∧_∧　ババババ\n（ ・ω・)=つ≡つ\n（っ ≡つ=つ\n`/　　)\n(ノΠＵ\n何回閉じても無駄ですよ～ww\nm9（＾Д＾）プギャー！！")
}
```

これは実際にこの事例で扱われたJavaScriptのソースコードである
ただただアラートループである:thinking:

ソースは解説するまでもなく、JavaScriptを採用したアラートを表示し続けるだけであり、これ単体ではWebサイトに無数にある悪質なアフィリエイトと比べると大した影響はない
(これについてはCoinhive事件などもあげられる)

---

```window.alert```はダイアログを閉じるまでは処理が進まないので、このプログラムはブラウザの動作に影響を与えるものではない

実際に実行すると<a href="https://hamukazu.github.io/lets-get-arrested/" target="_blank">これ</a>が表示されるだけである

これらと似たようなスクリプトは、悪質なアフィリエイトにも採用されており、そちらが取り締まられる前例があるのであるば一考の予知があるが、その前例も存在していない

それらを加味すると起訴猶予処分どころか、不正指令電磁的記録供用未遂で検挙が行われることすら懐疑的だ

Winny事件、Coinhive事件、Wizard Bible事件同様、日本のグローバルエンジニアへの道を閉ざす一因とならざるを得ない

--- 
アラートループにおける検証については以下を参照してください

**無限アラート事件の何が問題なのか考察してみた**
https://qiita.com/yuta0801/items/e6ed71a905e66c307046

**無限アラートは不正プログラムとして逮捕されるらしいので警察にゴールドバッハ予想を証明してもらおう**
https://qiita.com/yuta0801/items/82872d551caf47f2c7af

**Yahooニュースに無限ループを見つけた**
https://qiita.com/querykuma/items/a2deb09b634927be3206


---

# 反響(ITリテラシーに欠けた人物)
2019年3月5日

スマイリーキクチは補導の報道を受けて、ネット犯罪であることを前提にして
**「中1の少女が簡単にネット犯罪に手を染めてしまう。もうゲーム感覚なんでしょうね。この現実を大人がどのように受け止めればよいのか。。。」** 
と[ツイート](https://archive.fo/9lUgN)し、批判が殺到(推定無罪の原則)

小学生未満のリテラシーであることを自覚した上での発言だと思われるが、それを込みにしても教養が欠けているように感じられる

---

# 反響(有名エンジニアや教授等)

3月6日
JavaScriptの生みの親であるBrendanEichは、
 * [**「Chromeの初版よりも10年も前にリリースされたNetscape 4でもユーザーがループするJavaScriptをキルすることができた。」**](https://twitter.com/BrendanEich/status/1102953296719802369?s=20&t=7Vl3muWeyq2ecWyoAY3Oug)

 * [**「この事件の公判で専門家証人になるつもりでいる。これはウイルスなどではなく、犯罪扱いされるべきではない。もしブラウザがユーザーに制御を取り戻させなかったのならブラウザメーカーを投獄する 」**](https://twitter.com/BrendanEich/status/1104170683045564416?s=20&t=EU2SlJ8REw81YNe2TJ4P7g)

等ツイートした。

---
 ### [BrendanEich](https://ja.wikipedia.org/wiki/%E3%83%96%E3%83%AC%E3%83%B3%E3%83%80%E3%83%B3%E3%83%BB%E3%82%A2%E3%82%A4%E3%82%AF) [Netscape 4](https://ja.wikipedia.org/wiki/Netscape%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA)について

**ブレンダン・アイク**
Netscape Communications Corporationに転職後Netscape Navigatorを起源にもつ、世界で、もっとも使われているスクリプト言語**JavaScript**の開発者 JSの生みの親ともいわれる
現在ではJavaScriptだが、開発当初はLiveScriptであった

1998年に[mozilla.org](https://www.mozilla.org/ja/)を創設([Firefox](https://www.mozilla.org/ja/firefox/new/)ブラウザの開発元)
2005年にMozilla CorporationにてCTOとなる
現在はBrave Softwareを設立し、[Brave](https://brave.com/ja/)と呼ばれるプライバシー保護に長けたブラウザを開発している

---

**NetScape 4**
Firefoxの前進となったであろうMozilla社のブラウザ
Windows 95普及以前のバージョン3.0をリリースした1996年にはブラウザ全体の70%のシェアを誇っていた
最新版のリリースノートは、
`Netscape Navigator 4.08 – 1998年11月9日 (16bit版Windowsと68k Macintoshの最終リリース)`
となっている

つまり，兵庫県警は2000年代ですらない、16bitのコンピュータが主流の時代のブラウザの機能に負けたと煽られたということになる
**しかし、コレがエンジニア敗戦国の実情なのである**
(Winnyにおいても同じことがいえる)

---

# [みんなで逮捕されようプロジェクト](https://github.com/hamukazu/lets-get-arrested/blob/master/README.ja.md)

当時もっともGihubにて盛り上がったリポジトリの1つといって間違いないでしょう
ただの30ヶ国語に翻訳された`README.md`に150を超えるコミット、4000近いStar、1000を超えるForkなどが付いた
このリポジトリの特徴的なところは、これを使って逮捕されれば最良の結果を得られる部分で、forkし、gh-pagesブランチを切ればすぐにアラートループのWebサイトの設置が可能
現在までのところ検挙率は0だが、今後検挙される可能性があると思うと、おびえて日中しかソースコードが書けないという状況であり、これは改善していく必要がある

---

これに対し、兵庫県警は「自分の子どもにもそんなことが言えるのか」と反発したが、とてもではないが第三者から見ても理解可能な回答ではないと感じる
 * [「みんなで逮捕されようプロジェクト」がネット上で拡散中～サイバー犯罪対策課は「自分の子どもにもそんなことが言えるのか」と反発](https://www.data-max.co.jp/article/28329)

神奈川県警のCoinhive事件にしても似たような発言をしていたが、とても正気だとは思えない
* [「お前やってることは法律に引っかかってんだよ！」　コインハイブ事件、神奈川県警がすごむ取り調べ音声を入手](https://nlab.itmedia.co.jp/nl/articles/1902/28/news005.html)

---

# 結論
日本の警察の内部事情はとてもではないが透明性を保持できている、または教育がされているとは言い難い状態であることがわかると思う

現Googleの社員(Google Japanではない)である[Mariko Kosaka氏](https://twitter.com/kosamari)が当時この件について[言及していた](https://www.itmedia.co.jp/news/articles/1903/07/news071.html)が、プロを雇って1から教育するべきなのではないかと考えるが、埼玉県警の募集要項を見ても、なぜそこまでセキュリティに関して適切な知識をつけることに保守的になるのかがいまいち把握できかねる

現在のところはそれに連なる事件は起きていない(はず)だが、果たして今後も起こらないかといえばNoだろう。

---

不正指令電磁的記録のあいまいな定義もこれらを加速させている
海外では詳細に定めている国が多いが、日本では2013年以来それらを取り巻く法律は変更されておらず、依然としてあいまいであり、今後はたして改善される見込みがあるかは不明なのだ

このレポートを見ている、あるいはURLを共有しただけで検挙される可能性がある、そして検挙された事件同様アラートループへのURLが張られているこのレポートが世の中に出ているだけで投稿者が逮捕される可能性がある

**そう考えると現状の恐ろしさを体感できるのではないだろうか?**

---

# 文献およびソース
1. [Wikipedia:アラートループ事件](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%83%A9%E3%83%BC%E3%83%88%E3%83%AB%E3%83%BC%E3%83%97%E4%BA%8B%E4%BB%B6)
2. [横浜パーク法律事務所:アラートループ事件の被疑者２名に対する起訴猶予処分を受けて](https://www.yokohama-park-law.com/news/20190529.html)
3. [加藤公一(はむかず):みんなで逮捕されようプロジェクト](https://github.com/hamukazu/lets-get-arrested/blob/master/README.ja.md)
4. [ars TECHNICA:JavaScript infinite alert prank lands 13-year-old Japanese girl in hot water](https://arstechnica.com/tech-policy/2019/03/japanese-police-charge-13-year-old-girl-for-infinite-javascript-popup-prank/)
5. [Wikipedia:ブレンダン・アイク](https://ja.wikipedia.org/wiki/%E3%83%96%E3%83%AC%E3%83%B3%E3%83%80%E3%83%B3%E3%83%BB%E3%82%A2%E3%82%A4%E3%82%AF)
6. [Wikipedia:Netscape Navigator](https://ja.wikipedia.org/wiki/Netscape_Navigator_(%E3%83%8D%E3%83%83%E3%83%88%E3%82%B9%E3%82%B1%E3%83%BC%E3%83%97%E3%82%B3%E3%83%9F%E3%83%A5%E3%83%8B%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%BA))

その他、ブログ記事や詳細などはそれぞれハイパーリンクを参照

---

# 最後に
2019年はエンジニアにおいて、いかに日本が遅れをとっているかを理解させられた年かを理解すると同時に、今後忘れてはいけないことであるためこのレポートを記載した(かなり横道逸れているが)

静的ホスティングサービスであるGithub Pagesを使用しているため、Githubが閉鎖しない限りは半永久的に購読が可能
SlidevからMarp-cliへ乗り換えて初の投稿であるため、画像等がなくテーマ等いろいろ拙いのはご了承ください
issueに関しては[コチラ](https://github.com/Katsuyuki-Karasawa/1st-marp-ghpages/issues)へ

Portfolio --> https://katsuyuki-karasawa.pages.dev/
