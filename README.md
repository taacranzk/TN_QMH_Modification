# TN_QMH_Modification
LabVIEWのQueued Message Handlerをベースに手を加えたものです。

- LabVIEW 2026 Q3で作成
- 2020で読み取れるようには保存

手を加えたところ
#### Launcher.vi
このVIをスタートVIにする。

#### Create All Message Queues.vi
All Message Queues.ctlのメッセージキューの数を変更したあとにVI Script - Set Message Queue.viを実行すると自動配線する。

#### Close All Message Queues.vi
すべてのメッセージキューを1つのVIで破棄する。

#### User Event - Stop.lvlib
ユーザーイベントをタイプ定義クラスタにする。

#### Enqueue Message - Malleable.vim
メッセージのエンキューをMalleabel VIにする。

#### VI Script - Set Message Queue.vi
All Message Queues.ctlのメッセージキューの数を変更したあとにこのVIを実行すると、Create All Message Queues.viに反映される。

#### VI Script - Copy Templete MHL.vi
All Message Queues.ctlのメッセージキューの数を変更したあとにこのVIを実行すると、MHL TempleteにあるMHL.lvlibをLoopフォルダにコピーして名前をメッセージキュー.lvlibにする。
削除は手動。エラー配線などをちゃんとしていないですし、バグがあるかもしれません。
