# metafeed

metafeedは、Podcastにテキストやリンク等のメタデータを埋め込む仕組みです。

現在、metafeedの具体的な実装は公開されていません。

- [metafeedの仕組み](how-it-works.md)
- [metafeedを配信する方法](hosting.md)
- [metafeed対応アプリ](player.md)

## Show notes tags

"Show note tags" はPodcastにテキストまたはリンクを埋め込むことができるmetafeedの機能です。

- 多くのPodcastでは、すでにShow notesにたくさんのリンクを記載しています。[metafeed hub](hosting.md)を使えば、すでにある説明文やチャプターからTagを自動生成できます。

- 現状では [metaplayer](player.md) のみが対応しており、SpotifyやApple Podcastなどでは無視されます。

- 対応アプリでは、Tagが付与されたPodcastを再生する時に無音の通知を送ります (デフォルトの挙動)。

- 通知をタップすると、対応アプリ内のブラウザでリンクが開かれます。これは単なるリンクですが、埋め込むリンクの種類によって、様々なことができます。
  - お便り募集フォームを開く
  - サポーターを募集する
  - 音楽を聴く、YouTubeの動画を開く、他のPodcastを聴く
  - スポンサーのWebサイトを表示する

- ただし、どの場合でも、リスナーに何かを強制することはできません。
リスナーは、番組ごとにタグをどのように表示するかを選べます。気付きやすいように振動や音を鳴らしたり、エピソードの最後にまとめて通知したり、あるいは全く通知しないこともできます。
エピソードの再生画面ですべてのタグを見ることもできます。他のPodcastへのタグを辿ることもできます。
また「Do not disturb (おやすみモード・集中モード)」などを使っているユーザには通知は送られません。

Shownotes Tagはmetafeedの唯一の機能です。
metafeedは、あるPodcastで配信されている各エピソードについている全てのtagを、Webサーバとして配信する仕組みです。
metafeedを持っていないPodcastに対しては、[metafeed hub](hosting.md)が、自動生成された仮のmetafeedを配信できます。

## 実現できること

### インタラクティブな Show notes

- リスナーが、紹介されている本や論文や画像・動画などを簡単に開くことができます。例えば、旅行について語るPodcastで、現地で撮った写真アルバムを紹介できます。

### ユーザとのコミュニケーション

- Show notes tagを使うことで、例えば「ハッシュタグを付けてTwitterに投稿することを促す通知を送る」「エピソード終了30秒前に感想フォームのお知らせを送る」ことができます。リスナーは、通知で受け取るか、手が空いた時にアプリ内でまとめて確認するか、あるいは全く受け取らないかを番組ごとに選べます。

### オープンな Music + Talk

- Show notesを使えば、Spotifyの「Music + Talk」と似た機能を、Spotify以外のプレイヤーで、また他のコンテンツ (Spotify, Apple Music, Prime musicやYouTube) について実現できます。Spotifyの「Music + Talk」に比べると面倒でスムーズではない体験ですが、Spotifyなどのアプリに誘導せず音楽やYouTube、Podcastなどのコンテンツを埋め込めるオプションを好む方向けの機能です。

## metafeedを使ってみたい

現在、metafeedは提案段階であり、具体的な実装は公開されていません。

- あなたがPodcast配信者なら、[metafeed hub](hosting.md)を使って、metafeedを簡単に編集・配信できるようになります。
- あなたがリスナーなら、[metaplayer](player.md)であらゆるPodcastを聴くことができるようになります。