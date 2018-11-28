# このソフトウェアについて

　Qt5学習。QtでSQLite3を使う。QSqlTableModelを使ってみた01。

* `QSqlTableModel::record()`にてテーブル定義から作られたQSqlRecord(QsqlField)が取得できた

## 前回まで

* https://github.com/ytyaru/Cpp.Qt.Widget.QtSqlTableModel.20181128180000
* https://github.com/ytyaru/Cpp.Qt.Widget.QtSqliteDb.20181128160000
* https://github.com/ytyaru/Cpp.Qt.Widget.QtSqliteDb.20181128120000
* https://github.com/ytyaru/Cpp.Qt.Widget.QSql.SQLite3.Transaction.20181128070000
* https://github.com/ytyaru/Cpp.Qt.Widget.QSql.SQLite3.Class.20181127180000
* https://github.com/ytyaru/Cpp.Qt.Widget.QSql.SQLite3.Class.20181127170000
* https://github.com/ytyaru/Cpp.Qt.Widget.QSql.SQLite3.Class.20181127160000
* https://github.com/ytyaru/Cpp.Qt.Widget.QSql.SQLite3.Class.20181127130000

## コード抜粋

```cpp
QSqlRecord rec = model.record();
rec.setValue("Memo", QVariant("あああ"));
rec.setValue("Created", QVariant("1999-12-31 23:59:59"));
model.insertRecord(0, rec);
```

　`QSqlTableModel::record()`にてテーブル定義から作られたQSqlRecord(QsqlField)が取得できる。

## Qt要素

* http://doc.qt.io/qt-5/qsql.html
    * http://doc.qt.io/qt-5/qsqldatabase.html
    * http://doc.qt.io/qt-5/qsqlquery.html
    * http://doc.qt.io/qt-5/qsqlerror.html
    * http://doc.qt.io/qt-5/qsqltablemodel.html
    * http://doc.qt.io/qt-5/qsqlrecord.html
    * http://doc.qt.io/qt-5/qsqlfield.html

# 開発環境

* [Raspberry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi) 3 Model B+
    * [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) GNU/Linux 9.0 (stretch) 2018-06-27
        * Qt 5.7.1

## 環境構築

* [Raspbian stretch で Qt5.7 インストールしたもの一覧](http://ytyaru.hatenablog.com/entry/2019/12/17/000000)

# ライセンス

　このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

## 利用ライブラリ

ライブラリ|ライセンス|ソースコード
----------|----------|------------
[Qt](http://doc.qt.io/)|[LGPL](http://doc.qt.io/qt-5/licensing.html)|[GitHub](https://github.com/qt)

* [参考1](https://www3.sra.co.jp/qt/licence/index.html)
* [参考2](http://kou-lowenergy.hatenablog.com/entry/2017/02/17/154720)
* [参考3](https://qiita.com/ynuma/items/e8749233677821a81fcc)
