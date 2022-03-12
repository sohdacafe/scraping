# チートシート

### タグを指定して要素を取り出す
tag = soup.find('h2')
a_tag = soup.find('a')
a_tag.text # text属性
a_tag['href'] # a_tagのhref属性を表示

### HTMLの属性を指定して要素を取り出す
attr = soup.find(id = 'xxxx')
attr = soup.find(class_ = 'xxxx')

### 複数要素の取り出し
tags = soup.find_all(タグ名)
for tag in soup.find_all(タグ名):
    print(tag)

tags = soup.find_all([タグ名a,タグ名b,タグ名c]) # タグ名をリストにして指定することも可

for span in soup.find_all('span', class_='info-access'): #spanタグを探し出す

### パターンに一致した要素の取り出し
変数 = re.compile(正規表現)

pattern = re.compile('h[1-4]')
for h_tag in soup.find_all(pattern) :
    print(h_tag) #h1~h4タグのものを探し出す

pattern = re.compile('フラワー|Flower|flower')
for h_tag in soup.find_all(string=pattern) : #stringにpatternを指定して、一致するものを探す

for h_tag in soup.find_all('h2', string=pattern) : #h2またはstring=patternに一致するものを探す。組み合わせも可







