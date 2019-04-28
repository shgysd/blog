---
title: Hello, Gatsby.js
date: "2019-04-28"
description: "Gatsbyを触ってみての所感"
---

最近Twitterを始めて(今更すぎるが)、独自ドメインも取得したのでついでにBlogを始めようと思い
Mediumを使おうと考えていたがGatsbyを試したかったので使ってみた。

### いいところ
- Markdonwで書ける
- デプロイが楽(とか思ってたら早速ハマった)
- Reactで出来てるらしい

### わるいところ
- Blogやったことないからわからん

###なんでGatsby?

[ダン先輩](https://overreacted.io/)が使ってたから使ってみただけ。
関係ないけどReactやってる人は先輩のブログ読めばいい事あるかもですね。  
  
  
**既に満足感があるのでそのうち何かちゃんと書く**


### 追記
---

index.mdを書き換えてpushしたらいきなり怒られた。
```
5:10:05 PM:   GraphQL request (18:13)
5:10:05 PM:   17:             title
5:10:05 PM:   18:             description
5:10:05 PM:                   ^
5:10:05 PM:   19:           }
5:10:05 PM: - Unknown field 'description' on type 'MarkdownRemarkFrontmatter'.
5:10:05 PM:       file: /opt/build/repo/src/templates/blog-post.js
```
descriptionがねえ！って怒ってるけどこっちはなんのことがわからねえ！
ググっても出てこないので適当に追加してみた。
  
**結果**
```
---
title: Hello, Gatsby.js
date: "2019-04-28"
description: "Gatsbyを触ってみての所感"// この行が必要
---
```
  
`gatsby-starter-blog` で生成した時はこんなの無かったじゃねーかぶっ**すぞ！

   