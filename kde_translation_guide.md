---
title: KDE の日本語翻訳ガイド
date: 2026-01-26
---

## はじめに

これは、10数年ぶりに KDE を翻訳したときの作業メモです。
公式の情報は[こちら](https://jp.kde.org/community/getinvolved/translation/)。

## 翻訳ファイルをダウンロード

翻訳ファイルはこちらに置かれています。
[https://websvn.kde.org/trunk/l10n-support/ja/summit/messages/](https://websvn.kde.org/trunk/l10n-support/ja/summit/messages/)

「ark」を翻訳する場合は上のページにある「ark」をクリック。
「ark.po」の右側にある Rev 番号をクリック。
「download」を右クリックして「名前を付けてリンク先を保存」。

poedit などの翻訳アプリで「ark.po」を翻訳。
30分ほど翻訳したらいったんやめて、次のステップに進んでください。なにか間違いがあったとき、2時間分の作業をやり直すのはつらいものです。
全訳にこだわる必要はありません。まれにしか出ないエラーメッセージは後回しで良い。メニューや設定を先に翻訳すると、快適性が格段に上がります。

## メッセージを実際のアプリで表示

翻訳したメッセージをインストール。

```
msgfmt ark.po -o ark.mo
sudo cp ark.mo /usr/share/locale/ja/LC_MESSAGES/
```

アプリを再起動して、翻訳が反映されているか確認してください。

## 翻訳する際の注意

- 「S&ync」は「同期(&Y)」のように翻訳します。「(&Y)」はショートカットキー
- 英単語の前後には半角スペースを置きます (例: この Plasma は)
- かっこ () は半角です
- カタカナ語の語尾は伸ばしません (OK: ディレクトリ, NG: ディレクトリー)

注意事項を過剰に気にする必要はありません。気軽に翻訳してください。「ディレクトリー」と翻訳した場合でも、「ディレクトリ」への置換は一瞬でできます。

## 翻訳したファイルをメーリングリストに送付

メーリングリストに送付する場合は、[こちら](https://mail.kde.org/mailman/listinfo/kde-jp)にメールアドレスを入力して、メーリングリストへの入会を申し込んでください。名前とパスワードは省略可能。
退会するときは同じページに「Kde-jp からの退会」のボックスがあるので、メールアドレスを入力。入会も退会も数分で自動的に処理されます。

入会したら ```kde-jp@kde.org``` に次のようなメールを送ってください。

```
件名
翻訳しました: ark.po

本文
ark.po を翻訳しました。マージをお願いします。
```

「ark.po」を圧縮してメールに添付。

KDE のコミッタがファイルを確認して、KDE の公式リポジトリにマージします。何日か待ってください。

## Transifex などに移行する予定は？

英語フォーラムで「Weblate に移行する予定はありますか？」という質問が出ていますが、2023年8月時点で[その予定はない](https://discuss.kde.org/t/any-plans-to-move-to-weblate-for-translation/3415)とのこと。
KDE の翻訳者は KDE のユーザからしか生まれませんが、ほとんどの KDE ユーザにとって、今の翻訳方法は[困難だと思う](https://www.reddit.com/r/kde/comments/1024y46/any_plans_take_localisation_of_kde_to_a_better/?tl=ja)。ここに書いたことを調べて、翻訳アプリの使い方を覚えて、メーリングリストでやり取りしないといけない。2024年9月の時点で、活発に日本語翻訳をしている人はゼロでした。

翻訳のしやすさと既存の翻訳の完成度を求めるなら、デスクトップ環境は [LXQt](https://translate.lxqt-project.org/languages/ja/) / [Xfce](https://explore.transifex.com/xfce/) / [Budgie](https://explore.transifex.com/buddiesofbudgie/) などが良いと思います。KDE のようにメッセージ数が膨大ではないし、翻訳に Transifex や Weblate を使用しているので、ブラウザでプロジェクトページを開くだけで翻訳できる。

[HOME](index.html)
