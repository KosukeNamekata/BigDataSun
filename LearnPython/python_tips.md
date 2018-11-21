
## 便利なpythonのコードをまとめていく

## ある変数の正体を調べたいとき： print, type, dir

print関数を使って、変数の値を調べることができます。
また、type(x)は、xの型を返す関数です。たとえば、次のプログラムを実行すると

```
x=4.2
print(type(x))
```

次のような出力が帰ってきます。このことから、変数ｘの値は4.2で、その型は’float’であることがわかります。（floatは、pythonで実数を表現するのに通常つかわれる型です。）

```
4.2
<type 'float'>
```

さらに、dir(x)は、xの持っているメソッドを全て表示してくれます。

```
x="deep learning"
print(type(x))
print(dir(x))
```

```
<type 'str'>
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

は、次のような結果になります。

```
Deep learning
['deep', 'learning']
doop loarning
['d', '', 'p l', 'ar', 'i', 'g']
```

## appendとextendの違い...
・appendは、　　

・extendは、





