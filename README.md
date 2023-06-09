## Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
### リモートリポジトリ
  * ネット上にソースコードをアップできる専用のサービスの一種、GitHubがこれに該当する。
  * また、開発中のソースコードの大元をここで保管、メンバーはここからソースコードを取得して開発に参加できる。
  * ソースコードの修正、マージなどの変更箇所も閲覧できる。

### ローカルリポジトリ
  * 作業編集はWindowsの場合はGitBASHが必要。
  * リモートリポジトリから取得したソースコードを自身の端末で保管する場所。
  * リモートリポジトリとは独立しており、必要に応じてソースコードの開発・修正・変更などを記述していく。
  * ローカルでしたファイルなどはリモートリポジトリには含まれていないため、都度リモートリポジトリに上げる必要がある。

## プッシュとマージの違いは何でしょうか？
### プッシュ
  * ローカルでの編集内容をリモートリポジトリに上げること。
  * 基本は大元のソースコードから枝切りしたbranchに対してプッシュする。

### マージ
  * 大元の幹（ソースコード）に対して各ブランチで編集した内容を取り込むこと。
  * リモートリポジトリでのマージは基本的にプロジェクトリーダー等の決められた人だけがマージを行う。

## コミットとプッシュの違い
### コミット
  * 編集した内容をローカルリポジトリ内で指定したbranchに反映させる事。

### プッシュ
  * ローカルリポジトリにある各ブランチをリモートリポジトリにある各ブランチに反映させる事。

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
* 一目見て何を編集したか分かるように、どのファイルにどんな編集を加えたのかを記載する。
* コミットの書き方も意識する。特に３行ルールが見やすい。1行目はcommit内容の要約、２行目は空行、３行目に内容。
* prefix（接頭辞）の使用。
* 例　fix（バグ修正）add（新規機能・新規ファイル追加） update(バグではない機能修正)等
* prefixには絵文字もある


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
* 編集した内容をローカルリポジトリ内で自分でレビューをしてマージをするか、プルリクエストに対応する担当者がレビューをしてリモートリポジトリ内でマージするかの違いがある。特にプルリクエストからマージをした方がバグの発生を抑えることができる。

### 各マージのフロー
#### ローカル
  * ブランチを幹にマージ→リモートリポジトリにプッシュ

#### プルリクエスト
  * ローカルのブランチをリモートリポジトリのブランチにプッシュ→プルリクエスト→幹にマージ


## コンフリクトを起こしてしまった場合、どう対処すべきですか？
### 対処法は３つ
* 先にマージされた変更内容を取り込む。
* 後にマージされようとしている内容を取り込む。
* どちらの内容も取り込む。

* 最後のどちらも取り込む場合はエディタを使用してそれぞれの変更したい内容を記述した上で上書きする。また、コンフリクトが発生した場合は作業内容をコミットしておく。