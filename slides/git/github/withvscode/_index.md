+++
title = "github を Visual Studio Code から使う"
date = 2022-04-13T15:52:32+09:00
outputs = ["Reveal"]
[reveal_hugo]
custom_theme = "themes/asagao-tech.css"
margin = 0.2
+++

{{< slide template="simple-grey" >}}

まずは VS Code を立ち上げてみます。
{{< figure src="Screenshot from 2022-04-13 15-35-53.png" width="60%" link="Screenshot from 2022-04-13 15-35-53.png" >}}

この例では Linux で立ち上げていますが、Macintosh でも Windows でも
たぶん同じだと思うよ。

VS Code についての詳細は[こちら](/slides/vscode/install/)を参照

---

まずは試しに Asagao-Web-Content を例に上げます。

ここでは

#
{{< fragment >}} すでに git clone されている {{< /fragment >}}

#
{{< fragment >}} という前提で進めます {{< /fragment >}}

---

Asagao-Web-Content のディレクトリ(フォルダ)を開くと、
信頼しますか？と聞かれます。

{{< figure src="Screenshot from 2022-04-13 15-37-28.png" width="60%" link="Screenshot from 2022-04-13 15-37-28.png" >}}

ここでは、このプロジェクトを信頼するで進めます。

---

開くと左のアクティビティバーにエクスプローラと git が配置されているのがわかります。

{{< figure src="Screenshot from 2022-04-13 15-37-50.png" width="60%" link="Screenshot from 2022-04-13 15-37-50.png" >}}


---

アクティビティバーの拡大図です。
{{< figure src="activity-bar.png" >}}

- アクティビティバー: アイコンの列
- サイドバー: アイコンの列の右(ここではエクスプローラー)

---

エクスプローラーのアイコンをクリックしてファイル構成を見ます。

{{< figure src="Screenshot from 2022-04-13 15-38-02.png" width="60%" link="Screenshot from 2022-04-13 15-38-02.png" >}}

---

ここではコンテンツを一個仮に作ってみます。

posts/2022 を選択します。

{{< figure src="Screenshot from 2022-04-13 15-38-28.png" width="60%" link="Screenshot from 2022-04-13 15-38-28.png" >}}

---

04130 というディレクトリを作ります。(右クリックでメニューが出ます)

- 4/13 の 0 番目のコンテンツの意味(Asagao のローカル命名ルール)

{{< figure src="Screenshot from 2022-04-13 15-38-42.png" width="60%" link="Screenshot from 2022-04-13 15-38-42.png" >}}

---

次にファイルを作ります。(右クリックでメニューが出ます)

{{< figure src="Screenshot from 2022-04-13 15-38-52.png" width="60%" link="Screenshot from 2022-04-13 15-38-52.png" >}}

---

index.md というファイルを作りました。
このファイル名は Hugo というシステムのルール。

{{< figure src="Screenshot from 2022-04-13 15-39-06.png" width="60%" link="Screenshot from 2022-04-13 15-39-06.png" >}}

---

新しくファイルを作ったので
 
- {{< fragment >}} エクスプローラーがセーブされていないファイル数 {{< /fragment >}}
- {{< fragment >}} git が変更されているファイル数 {{< /fragment >}}

#
{{< fragment >}} を明示します。{{< /fragment >}}

{{< figure src="Screenshot from 2022-04-13 15-40-04.png" width="60%" link="Screenshot from 2022-04-13 15-40-04.png" >}}

---

index.md に Hugo の規則に従ってコンテンツ内容を記述します。


{{< figure src="Screenshot from 2022-04-13 15-42-26.png" width="60%" link="Screenshot from 2022-04-13 15-42-26.png" >}}

---
# ほんとうは

Visual Studio Code に Hugo 用のプラグインを入れると
手間が省けるらしい。

---
# ついでに書くと

```HUGO
<!-- more -->
```

までがサマリー。
その後が本文。

---

本文も書きます。
セーブも忘れずに

{{< figure src="Screenshot from 2022-04-13 15-43-08.png" width="60%" link="Screenshot from 2022-04-13 15-43-08.png" >}}

---

サイドーバーで git をクリックすると
add と commit と更新のアイコンがあるのがわかります。

{{< figure src="vscode-github-icon.png" >}}

---

まずは add をしてみましょう。add 用の icon をクリックします。

{{< figure src="Screenshot from 2022-04-13 15-43-40.png" width="60%" link="Screenshot from 2022-04-13 15-43-40.png" >}}

---

ステージされている変更に _index.md が移りました。

(非常に分かりづらいのですが、、、)

{{< figure src="Screenshot from 2022-04-13 15-43-53.png" width="60%" link="Screenshot from 2022-04-13 15-43-53.png" >}}

---

次に commit の icon をクリックします。

本文の _index.md の上に commit のための

コメント入力欄が現れました。

{{< figure src="Screenshot from 2022-04-13 15-44-52.png" width="60%" link="Screenshot from 2022-04-13 15-44-52.png" >}}

---

「テスト的に commit します」

と入力しました。

{{< figure src="Screenshot from 2022-04-13 15-45-18.png" width="60%" link="Screenshot from 2022-04-13 15-45-18.png" >}}

---

リターンすると commit 完了です。

次に更新の icon をクリックします。

{{< figure src="Screenshot from 2022-04-13 15-45-31.png" width="60%" link="Screenshot from 2022-04-13 15-45-31.png" >}}

---

更新は

- {{< fragment >}} push した上に {{< /fragment >}}
- {{< fragment >}} pull もします {{< /fragment >}}

#

{{< fragment >}} つまり同期をとってくれます。 {{< /fragment >}}


{{< figure src="Screenshot from 2022-04-13 15-46-19.png" width="60%" link="Screenshot from 2022-04-13 15-46-19.png" >}}

---

同期が取れたようです。

#
{{< fragment >}} もし、github.com 上での変更があれば {{< /fragment >}}

#
{{< fragment >}} 同時にその変更を {{< /fragment >}}

#
{{< fragment >}} ローカルにも {{< /fragment >}}

#
{{< fragment >}} 反映します {{< /fragment >}}

{{< figure src="Screenshot from 2022-04-13 15-46-13.png" width="60%" link="Screenshot from 2022-04-13 15-46-13.png" >}}

---

自動的に同期を取ることもできるようです。

私は「いいえ」を選択しました。


{{< figure src="Screenshot from 2022-04-13 15-46-39.png" width="60%" link="Screenshot from 2022-04-13 15-46-39.png" >}}

---

念の為 github.com を確認してみます。

反映していることが(コメントで)わかります。

{{< figure src="Screenshot from 2022-04-13 15-47-36.png" width="60%" link="Screenshot from 2022-04-13 15-47-36.png" >}}

