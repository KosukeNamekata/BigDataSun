
## 便利なpythonのコードをまとめていく

### ＊pythonは、全てがオブジェクト指向プログラム  
- pythonの変数、リストなどは、全てクラスによって定義された「**インスタンス**」と同じような機能を持ち、**多くのメソッドが用意されている**。


### ＊ある変数の正体を調べたいとき： type, dir

- type(x): xの型を返す関数です。たとえば、次のプログラムを実行すると

```
x=4.2
print(type(x))
```
```
<type 'float'>
```

- dir(x): xの持っているメソッドを全て表示してくれます。

```
x="deep learning"
print(dir(x))
```
```
['__add__', '__class__', '__contains__', ... , 'zfill']
```

ここから、xは’str’型(文字列型)であること、またcapitalize, split, replaceなどのメソッドを持っていることがわかります。
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
・appendは、　　

・extendは、





