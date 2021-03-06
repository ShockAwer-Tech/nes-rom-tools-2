■簡易説明

ロックマン2のROMイメージを読み込むことで、マップ・オブジェクトの配置などを編集できます。

以下、各タブ毎の機能の説明

[パレット]
ステージの描画に使われるパレットを編集します。

・パレットの編集
  左クリック -> パレットの色を選択色に変更
  右クリック -> 選択色をパレットの色に変更

・パレットアニメの編集
  フレーム総数       -> 0でパレットアニメ無効, 1〜4の範囲で選択
  アニメーション間隔 -> パレットが次のフレームに変わるまでの時間
  左クリック         -> パレットの色を選択色に変更
  右クリック         -> 選択色をパレットの色に変更


[32x32チップ]
マップ作成に使用する32x32チップを編集します。

・32x32チップテーブル
  左クリック         -> 32x32チップを編集対象チップに指定
  Ctrl + 右クリック  -> 32x32チップを1個コピー
  Ctrl + 左クリック  -> コピーした32x32チップを貼り付け
  Shift + 右クリック -> 16x16チップを選択チップに指定(右クリックのみでも同じ)
  Shift + 左クリック -> 選択16x16チップを貼り付け

・編集対象チップ
  イメージ上で左クリック           -> 選択16x16チップを貼り付け
  イメージ上で右クリック           -> 16x16チップを選択チップに指定
  属性ラベル上で左(右)クリック     -> チップ属性変更
  チップNoラベル上で左(右)クリック -> パレット変更

「CHR再読み込み」ボタン -> ROMイメージをバッファに再読み込みし、CHRを再描画


[マップ]
マップを編集します。

・マップ編集
  右クリック         -> 32x32チップを選択チップに指定
  左クリック         -> 32x32チップを貼り付け
  Ctrl + 右クリック  -> 1部屋分コピー
  Ctrl + 左クリック  -> 1部屋分貼り付け
  Shift + 左クリック -> マップ編集用グリッドの表示

「CHR再読み込み」ボタン -> ROMイメージをバッファに再読み込みし、CHRを再描画


[オブジェクト]
・オブジェクト編集画面
  オブジェクトを左クリック  -> オブジェクトを選択
  Ctrl + Shift + 左クリック -> オブジェクトを選択(ドラッグが無効化されるためオブジェクトを誤って動かしてしまう心配がありません)
  
  オブジェクトをドラッグ  -> オブジェクトを移動
  Ctrl + ドラッグ         -> オブジェクトを8ドット単位で移動
  Shift + ドラッグ        -> オブジェクトを4ドット単位で移動
  右クリック              -> ポップアップメニューを表示
  
  マウスがオブジェクト上にない状態でShift+左クリック -> オブジェクト編集用テキストボックスを表示
  
・オブジェクトの順序
  部屋単位で管理 -> オブジェクトの設置番号の計算を部屋単位で行う。オブジェクトのX座標で自動ソートが可能。
                    自動ソートを無効にしている場合、設置番号の横にあるボタンで順序を変更できます。
  自由順序       -> 部屋を越えてオブジェクトの順序を前後させたい場合に使用。
                    自動ソートが強制的に無効になります。設置番号の横にあるボタンで順序を変更できます。

(*)オブジェクトの編集はアンドゥ・リドゥの対象外となります


[スクロール]
・リストボックス
  スクロールデータを選択 -> 編集対象のスクロールデータを選択

・マップ上の記号の意味
  「>>」 -> 右に進行
  「→」 -> 右にスクロール
  「↓」 -> 下にスクロール
  「↑」 -> 上にスクロール


[復帰地点]
・復帰地点編集画面
  「値を自動計算」ボタン         -> 復帰部屋番号を元に他の値を計算します。
                                    スクロール番号、左端部屋番号、右端部屋番号は自動計算されません。
  「まとめて値を自動計算」ボタン -> そのステージの復帰地点データをまとめて計算します。
                                    スクロール番号、左端部屋番号、右端部屋番号は自動計算されません。
  
(*1)スクロール番号($3B30〜)、右端の部屋番号($3B3C〜)は自動計算されないため自力で値を設定してください。
(*2)復帰地点の編集はアンドゥ・リドゥの対象外となります


■iniファイルについて
各データ読み出しアドレスなどをiniファイルに出力します。
iniファイルを編集することでデータ読み出しアドレスを変更することができます。

・スタート地点に使用する復帰データについて
[LevelDataDefault]セクションのDefaultStartPoint[X]で各ステージのスタート地点に使用する
復帰データの番号を指定できます。
デフォルトでは、原作通り8ボスステージが0、ワイリーステージ1〜6が3となっています。


■更新履歴
09/08/16 スクロール編集画面に選択したスクロールに対応する左端・右端部屋番号を表示
         オブジェクト編集画面上で Shift+左クリック でオブジェクト編集テキストボックスを表示
09/08/14 (2)スクロール編集機能を追加
09/08/14 (1)「CHR読み込み」ボタンを追加、マップ編集画面上で Shift+左クリック でマップ編集用グリッドを表示
・・・



