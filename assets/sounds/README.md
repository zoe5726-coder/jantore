# assets/sounds — 効果音（SE）の一覧

R96（0.88.0 / build 20261024-01）で採用音源に切り替えた。
アプリは `SND_FILES`（jantore.html の SoundManager）に書いたファイル名だけを読む。
同じファイル名で上書きすれば、コードを変えずに音だけ差し替えられる。

## 採用音源（正式）

| ファイル | 元の素材名 | 提供元 | 取得元ページ | 元ファイルURL | アプリでの用途 | 共用 |
|---|---|---|---|---|---|---|
| select.mp3 | 決定ボタンを押す29 | 効果音ラボ | https://soundeffect-lab.info/sound/button/ | https://soundeffect-lab.info/sound/button/mp3/decision29.mp3 | 通常の選択・ボタン操作 | ― |
| correct.mp3 | 決定ボタンを押す5 | 効果音ラボ | https://soundeffect-lab.info/sound/button/ | https://soundeffect-lab.info/sound/button/mp3/decision5.mp3 | 正解 | ― |
| wrong.mp3 | 決定ボタンを押す42 | 効果音ラボ | https://soundeffect-lab.info/sound/button/ | https://soundeffect-lab.info/sound/button/mp3/decision42.mp3 | 不正解 | ― |
| lessonComplete.mp3 | 決定ボタンを押す27 | 効果音ラボ | https://soundeffect-lab.info/sound/button/ | https://soundeffect-lab.info/sound/button/mp3/decision27.mp3 | レッスンクリア | 全問正解と共用 |
| mission.mp3 | 決定ボタンを押す12 | 効果音ラボ | https://soundeffect-lab.info/sound/button/ | https://soundeffect-lab.info/sound/button/mp3/decision12.mp3 | デイリーミッション達成 | ― |
| themeComplete.mp3 | シャキーン1（ポーズを決める） | 効果音ラボ | https://soundeffect-lab.info/sound/anime/ | https://soundeffect-lab.info/sound/anime/mp3/shakin1.mp3 | テーマ制覇 | 連続日数の節目（3・7・14・30日）と共用 |

- ファイルはPOからの提供分をそのまま配置した。加工はしていない。
  - 長さ、音量差、無音部分もそのまま。
  - 音量バランスはアプリ内部の SND_GAIN で調整する。
- 提供時のファイル名は文字化けしていた（例：`________27.mp3`）。
  - 末尾の番号で素材と対応づけている（POの確認済み）。
  - 効果音ラボの元ファイルとのバイト照合はしていない。

| ファイル | MD5 | 長さ |
|---|---|---|
| select.mp3 | a57a8c53ca4311e8f709138684ddfafe | 1.10s |
| correct.mp3 | 2e47029ed21634c931170aa7f52e1f54 | 2.14s |
| wrong.mp3 | 465f3a9a340f45216f289a8fe2e63466 | 1.32s |
| lessonComplete.mp3 | 4499a3a8cfb6706da715d5535a786831 | 3.58s |
| mission.mp3 | 2d9fb68a81172c4be1eb13ebbb626d7f | 1.04s |
| themeComplete.mp3 | 8f66f7e1f82ccbc57ce24e912f87845a | 1.78s |

## ライセンス（確認日 2026-10-13）

確認先：https://soundeffect-lab.info/agreement/

規約の記載から確認できたこと：

- 個人、法人、公的機関を問わず、無料で使える（商用利用可）。利用報告はいらない。
- クレジット表記は任意（禁止ではない）。
- 操作音などとしてアプリに組み込むのは再配布にあたらない（音源ファイルがむき出しでも可）。
- 素材の再配布や販売、効果音そのものが主役になるコンテンツへの利用は禁止。
  - 効果音を自由に鳴らせるアプリや、フリー素材への組み込みも、ここに含まれる。
- 加工は可。ただし加工したものの再配布は不可。
- 効果音ファイルへの直リンク（効果音ラボのサーバー上のファイルを直接参照すること）は禁止。
  - このアプリは自前の assets から配信していて、直リンクはしていない。
- AI学習用データとしての利用は禁止。
- 規約は予告なく変わることがある。

このアプリの使い方は、学習アプリの操作音・演出音として、自前の assets で配信する形。規約の上記の範囲に入ると判断した。
有料版やアプリ内課金についての明記は、規約にはなかった。

## 仮音源（R96の対象外。変更していない）

| ファイル | 用途 | 状態 |
|---|---|---|
| discard.wav | 打牌音 | 仮音源。打牌音は別途選定 |
| streak.wav | ひとり麻雀の自己ベスト・ビンゴ・役図鑑など（soloEnd） | 仮音源。今後の整理の候補 |

## もう参照していない旧仮音源（消していない）

select.wav / correct.wav / wrong.wav / lessonComplete.wav / themeComplete.wav / streakMile.wav

- R96からアプリは読み込まない。
- 消すかどうかはPOが判断する。
- README_TEMPORARY.txt は、これら旧WAV一式についての説明（当時のもの）。
