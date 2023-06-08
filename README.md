## Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
### リモートリポジトリ
  *ネット上にソースコードをアップできる専用のサービスの一種、GitHubがこれに該当する。
  *また、開発中のソースコードの大元をここで保管、メンバーはここからソースコードを取得して開発に参加できる。
  *ソースコードの修正、マージなどの変更箇所も閲覧できる。

### ローカルリポジトリ
  *作業編集はWindowsの場合はGitBASHが必要。
  *リモートリポジトリから取得したソースコードを自身の端末で保管する場所。
  *リモートリポジトリとは独立しており、必要に応じてソースコードの開発・修正・変更などを記述していく。
  *ローカルでしたファイルなどはリモートリポジトリには含まれていないため、都度リモートリポジトリに上げる必要がある。

## プッシュとマージの違いは何でしょうか？
### プッシュ
  *ローカルでの編集内容をリモートリポジトリに上げること。
  *基本は大元のソースコードから枝切りしたbranchに対してプッシュする。

### マージ
  *大元の幹（ソースコード）に対して各ローカルで作成したbranchをリモートリポジトリの各ブランチに反映、そのブランチを幹に取り込ませること。
  *基本的にプロジェクトリーダー等の決められた人だけがマージを行う。

## コミットとプッシュの違い
### コミット
  *編集した内容をローカルリポジトリ内で指定したbranchに反映させる事。

### プッシュ
  *ローカルリポジトリにある各ブランチをリモートリポジトリにある各ブランチに反映させる事。

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
*一目見て何を編集・修正・変更・追加した内容が分かるように書く。


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
*編集した内容をローカルリポジトリ内で自分でレビューをしてマージをするか、プルリクエストに対応する担当者がレビューをしてリモートリポジトリ内でマージするかの違いがある。特にプルリクエストからマージをした方がバグの発生を抑えることができる。

### 各マージのフロー
#### ローカル
  *ブランチを幹にマージ→リモートリポジトリにプッシュ

#### プルリクエスト
　*ローカルのブランチをリモートリポジトリのブランチにプッシュ→プルリクエスト→幹にマージ


## コンフリクトを起こしてしまった場合、どう対処すべきですか？
### 対処法は３つ
*先にマージされた変更内容を取り込む。
*後にマージされようとしている内容を取り込む。
*どちらの内容も取り込む。

*最後のどちらも取り込む場合はエディタを使用してそれぞれの変更したい内容を記述した上で上書きする。また、コンフリクトが発生した場合は作業内容をコミットしておく。