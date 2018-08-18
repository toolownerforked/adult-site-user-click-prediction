# アダルトサイトの人気予想

具体的なアダルトサイトとは、`https://movie.eroterest.net/`。  

各動画のクリック数がカウントされているため、予想するタスクとしてやりやすい。  


## スクレイピングとデータ・セット

スクレイピング済みのファイル
 - https://www.dropbox.com/s/yzmvw2a9yp8kjhn/parsed.tar.gz?dl=0
 - https://www.dropbox.com/s/86h3h8zgpzrvjpz/imgs.tar.gz?dl=0
 

新規にスクレイピングする場合
 - https://github.com/GINK03/scraping-designs/tree/master/eroterest

## テキスト情報でからがクリック数を予想する

**単語にインデックスをふり、疎行列の変換の準備ファイルを作成**  

```
$ python3 preparation.py 
```

**疎行列を作成する**  
```
$ python3 bow_embed.py --mode=make_sparse
```

**DeepLearningに学習できるように密行列に変換**  
```
$ python3 bow_embed.py --mode=make_dense
```
