.. _walkthrough:

****************************************************************************************************
ドキュメントの作成手順
****************************************************************************************************
ドキュメントを作る工程の最初から最後までを実際に操作しながら説明します。

----

#. ドキュメントを保存するフォルダーを作る

   Sphinx はフォルダー単位でドキュメントを管理します。フォルダー内にドキュメントを構成する複数のファイルやフォルダーが配置されます。まず、これらを保存するフォルダーを作ります。今回は "C:¥Sphinx¥test" フォルダーを作りました。中身は空です。

   |

#. "Anaconda Powershell Prompt(Miniconda3)" を起動

   .. image:: img/2020-03-01_10h14_35.png

   |

   .. note::

      "Anaconda Powershell Prompt(Miniconda3)" と "Anaconda Prompt（Miniconda3)" はどちらを起動しても良いです。実行するコマンドの指定の仕方に少し違いがあります。

   |

#. 「ドキュメントを保存するフォルダーを作」で作成したフォルダーへ移動

   :command:`cd C:\\Sphinx\\test`

   .. image:: img/2020-03-01_10h20_41.png

   |

#. :command:`sphinx-quickstart` コマンドを実行

   " :command:`sphinx-quickstart` "コマンドを実行して Sphinx でドキュメントを作成するのに必要なファイルを作成します。

   .. image:: img/2020-03-01_10h25_53.png

   作成途中でいくつか質問されます。適当に回答しても、後で修正できます。

   > Separate source and build directories (y/n) [n]: 
      - ソースファイル用フォルダー（ source ）と HTML 用フォルダー（ build ）を分けるかどうかを指定します。
      - 分ける場合は ``y`` 、同じフォルダー内に作成する場合は ``n`` （デフォルト）を入力します。

   > Project name: 
      - プロジェクト名を入力します。
      - 入力した値はドキュメントのタイトル部分に表示されます。

   > Author name(s): 
      - 作者名を入力します。
      - 入力した値はドキュメントの (C) の後に表示されます。

   > Project release []: 
      - ドキュメントのリリース（版）番号を入力します。

   > Project language [en]:
      - ドキュメントの言語を入力します。
      - 日本語は ``ja`` を入力します。

   :command:`sphinx-quickstart` コマンドの実行後のフォルダーの状態です。

   .. image:: img/2020-03-01_10h28_34.png

   |

#. ドキュメントを作成

   ドキュメントを作成／修正します。今回はこの作業は省略します。

   |

#. HTML に変換

   " :command:`./make html` " コマンドを実行して HTML 形式の文書を作成します。

   .. image:: img/2020-03-01_10h42_17.png

   |

   .. note::

      "Anaconda Prompt（Miniconda3)" は" :command:`make html` "です。   
   
   |

#. 作成した文書を確認

   ブラウザーでドキュメント用フォルダー内の "build¥html" フォルダー内の "index.html" ファイルを開きます。今回は "C:¥Sphinx¥test¥build¥html¥index.html" を開きます。

   .. image:: img/2020-03-01_10h46_54.png

   "index.html" ファイルをブラウザーで開いた結果です。 :command:`sphinx-quickstart` コマンドを実行したときに入力した値が表示されています。

   .. image:: img/2020-03-01_10h47_51.png

.. note::

   「ドキュメントを作成／更新」、「 HTML に変換（ make html ）」、「確認」の繰り返しで文書を作成します。
