インストールの方法
==========================

1. Download ZIPからフォルダをダウンロードします。

2. ZIPファイルを解凍し以下の通りに配置します。   
`C: > Users > .nuke > gizmos > NormalizeDepth.gizmo`  
`C: > Users > .nuke > gizmos > NormalizeDepth_logo.png`

3. init.pyに以下のコマンドを追加する。  
```py
nuke.pluginAddPath('./gizmos')
```

4. menu.pyに以下のコマンドを追加する。
```py
nuke.menu('Nodes').addCommand('NormalizeDepth', "nuke.createNode( 'NormalizeDepth.gizmo')", icon ='NormalizeDepth_logo.png')
```

5. Nukeを再起動し、ツールバーにアイコンが表示されていればOK。


使用方法
==========================

1. Depthチャンネルを含んだノードにNormalizeDepthを接続する。  

2. ROIが画像サイズと合っていなければ、"Reset"を押して調整する。 

3. "start"を押すとポップアップメニューが表示されるので、フレームレンジを設定しOKを押すとシーンの解析が始まる。

4. "gamma"で後から微調整が可能。
