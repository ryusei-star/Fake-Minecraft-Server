# Fake Minecraft Server

<table>
	<thead>
    	<tr>
      		<th style="text-align:center"><a href="README.md">English</a></th>
      		<th style="text-align:center">日本語</th>
    	</tr>
  	</thead>
</table>

Minecraftサーバーを模倣するPython製サーバーです。  
サーバーPing（MOTD表示）に応答し、MOTD・バージョン・プレイヤー情報を表示します。  
プレイヤーは参加できません。

## 必要環境

- Python 3.8以上
- PyYAML

依存ライブラリのインストール：

```
pip install pyyaml
```

## 設定

`config.yml` を編集してください。  
存在しない場合は、起動時にデフォルト設定が自動生成されます。

```
ip: 0.0.0.0
port: 25565
motd: |
  §aFake Minecraft Server
  §7Welcome!
version_text: FakeMinecraftServer
kick_message: |
  このサーバーには参加できません。
  管理者にお問い合わせください。
server_icon: ''
max_players: 10
online_players: 0
```

## 使用方法

```
python3 main.py
```

- MinecraftクライアントからのPingに応答します。
- MOTD・バージョン・人数表示が反映されます。
- 接続・Ping・Kickはログに記録されます。
- 停止する場合は `Ctrl+C` を押してください。
