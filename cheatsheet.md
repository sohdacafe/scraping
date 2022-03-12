# チートシート

### タグを指定して要素を取り出す
tag = soup.find('h2')
a_tag = soup.find('a')
a_tag.text
a_tag['href'] # a_tagのhref属性を表示

### HTMLの属性を指定して要素を取り出す
attr = soup.find(id = 'xxxx')
attr = soup.find(class_ = 'xxxx')

# 複数要素の取り出し
tags = soup.find_all(タグ名)
for tag in soup.find_all(タグ名):
    print(tag)

