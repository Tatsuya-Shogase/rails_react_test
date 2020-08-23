# README

##【掲示板アプリ】
・登場人物：投稿者(匿名)、管理者  
・掲示板機能  
　-「カテゴリ」があり、上記ユーザーは「カテゴリ」ごとににテキストを投稿できる  
　-投稿するときは「名前／メールアドレス／件名／本文」が入力可能  
　→ただし、本文以外は任意項目  
　-一度投稿したテキストは編集／削除不可。ただし、投稿者だけ非表示にできる  
　　→非表示になった投稿は全員から見えない  
　-管理者は「カテゴリ」の追加／削除／編集ができる  

・管理機能  
　-管理者のみアクセス可能  
　-「カテゴリ」ごとに投稿数を確認できる  
　-「カテゴリ」の追加／削除／編集は管理機能で実施する  
　-非表示になった投稿も含め、「カテゴリ」ごとにすべての投稿を確認できる  


##DB構成  
Users  
  username, password, admin  

Categories  
  name  

Posts  
  session_id, name, mail, subject, text, visible, category_id(foreign_key)  


##環境  
RailsをAPIでインストールし、front_endディレクトリにReactをインストールしています。  
DBはsqliteを使用。  
migrationとseedsファイルは作成していますが、念のためsqliteファイルもpushしています。  
