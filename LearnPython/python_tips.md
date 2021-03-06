
## 便利なpythonのコードをまとめていく

### ＊pythonは、全てがオブジェクト指向プログラム  
- pythonの変数、リストなどは、全てクラスによって定義された「**インスタンス**」と同じような機能を持ち、**多くのメソッドが用意されている**。


### ＊ある変数の正体を調べたいとき： type, dir

- `type(x)`: xの型を返す関数です。たとえば、次のプログラムを実行すると  

- `dir(x)`: xの持っているメソッドを全て表示してくれます。

- xは’str’型(文字列型)であること、また`capitalize`, `split`, `replace`などのメソッドを持っていることがわかります。
メソッドや型の名前がわかれば、その使い方は「python str capitalize [検索]」などとして調べることができます。さっそく使ってみましょう。

```
x = ”deep learning”
print(x.capitalize())
print(x.split(" "))
print(x.replace("e","o"))
print(x.replace("e","n").split("n"))
```
```
Deep learning
['deep', 'learning']
doop loarning
['d', '', 'p l', 'ar', 'i', 'g']
```

### ＊リストへの操作：appendとextendの違い...
- **「pythonのリストは、インスタンス」**。numpyを入れないと、四則演算はできないが、様々なメソッドがビルドインされている。  

- `list.append(x)`: 　リストの末尾に要素を一つ追加します。a[len(a):] = [x] と等価です。

- `list.extend(x)`: イテラブルのすべての要素を対象のリストに追加し、リストを拡張します。a[len(a):] = iterable と等価です。

- `list.insert(i, x)`: 指定した位置に要素を挿入します。第 1 引数は、リストのインデクスで、そのインデクスを持つ要素の直前に挿入が行われます。従って、 `a.insert(0, x)` はリストの先頭に挿入を行います。また `a.insert(len(a), x)` は `a.append(x)` と等価です。

- `list.remove(x)`:　リスト中で、値 x を持つ最初の要素を削除します。該当する項目がなければエラーとなります。  

- `list.pop([i])`: リスト中の指定された位置にある要素をリストから削除して、その要素を返します。インデクスが指定されなければ、 `a.pop()` はリストの末尾の要素を削除して返します。この場合も要素は削除されます。 (メソッドの用法 (signature) で i の両側にある角括弧は、この引数がオプションであることを表しているだけなので、角括弧を入力する必要はありません。この表記法は Python Library Reference の中で頻繁に見ることになるでしょう。)

- `list.clear()`: リスト中の全ての要素を削除します。`del a[:]` と等価です。

- `list.index(x[, start[, end]])`: リスト中で、値 x を持つ最初の要素の位置をゼロから始まる添字で返します。 該当する要素がなければ、ValueError を送出します。任意の引数である start と end はスライス記法として解釈され、リストの探索範囲を指定できます。返される添字は、start 引数からの相対位置ではなく、リスト全体の先頭からの位置になります。

- `list.count(x)`: リストでの x の出現回数を返します。

- `list.sort(key=None, reverse=False)`: リストの項目を、インプレース演算 (in place、元のデータを演算結果で置き換えるやりかた) でソートします。引数はソート方法のカスタマイズに使えます。 sorted() の説明を参照してください。

- `list.reverse()`: リストの要素を、インプレース演算で逆順にします。

- `list.copy()`: リストの浅い (shallow) コピーを返します。a[:] と等価です。

