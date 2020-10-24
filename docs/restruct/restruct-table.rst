.. _restruct-table:

****************************************************************************************************
テーブル（表） : table ディレクティブ
****************************************************************************************************
| **【トピックス】**
| ・ :ref:`restruct-grid-table`
| ・ :ref:`restruct-simple-table`
| ・ :ref:`restruct-csv-table`
| ・ :ref:`restruct-list-table`
| ・ :ref:`restruct-complexity-table`
| ・ :ref:`restruct-width`
| ・ :ref:`restruct-table-header`
| ・ :ref:`restruct-table-title`

----

.. _restruct-grid-table:

グリッドテーブル
==================================================
.. code-block:: none

   +-------+-------+---------+
   | A     | B     | A and B |
   +-------+-------+---------+
   | False | False | False   |
   +-------+-------+---------+
   | True  | False | Flase   |
   +-------+-------+---------+
   | False | True  | False   |
   +-------+-------+---------+
   | True  | True  | True    |
   +-------+-------+---------+

+-------+-------+---------+
| A     | B     | A and B |
+-------+-------+---------+
| False | False | False   |
+-------+-------+---------+
| True  | False | Flase   |
+-------+-------+---------+
| False | True  | False   |
+-------+-------+---------+
| True  | True  | True    |
+-------+-------+---------+

----

.. _restruct-simple-table:

シンプルテーブル
==================================================
.. code-block:: none

   ====== ====== =======
   A      B      A and B
   False  False  False
   True   False  False
   False  True   False
   True   True   True
   ====== ====== =======

====== ====== =======
A      B      A and B
False  False  False
True   False  False
False  True   False
True   True   True
====== ====== =======

----

.. _restruct-csv-table:

CSV テーブル
==================================================
.. code-block:: none

   .. csv-table::
   
      "A", "B", "A and B"
      "False", "False", "False"
      "True", "False", "False"
      "False", "True", "False"
      "True", "True", "True"

.. csv-table::

   "A", "B", "A and B"
   "False", "False", "False"
   "True", "False", "False"
   "False", "True", "False"
   "True", "True", "True"

----

.. _restruct-list-table:

リストテーブル
==================================================
.. code-block:: none

   .. list-table::
   
      * - A
        - B
        - A and B
      * - False
        - False
        - False
      * - True
        - False
        - False
      * - False
        - True
        - False
      * - True
        - True
        - True

.. list-table::

   * - A
     - B
     - A and B
   * - False
     - False
     - False
   * - True
     - False
     - False
   * - False
     - True
     - False
   * - True
     - True
     - True

----

.. _restruct-complexity-table:

複雑なテーブル
==================================================
- グリッドテーブルを使用すると複雑なテーブルを作成できます。

.. code-block:: none

   +-----+-------+-------+--------+
   |     | A     | B     | Result |
   +-----+-------+-------+--------+
   | and | False | False | False  |
   +     +-------+-------+        +
   |     | True  | False |        |
   +     +-------+-------+        +
   |     | False | True  |        |
   +     +-------+-------+--------+
   |     | True  | True  | True   |
   +-----+-------+-------+--------+
   | or  | False | False | False  |
   +     +-------+-------+--------+
   |     | True  | False | True   |
   +     +-------+-------+        +
   |     | False | True  |        |
   +     +-------+-------+        +
   |     | True  | True  |        |
   +-----+-------+-------+--------+

+-----+-------+-------+--------+
|     | A     | B     | Result |
+-----+-------+-------+--------+
| and | False | False | False  |
+     +-------+-------+        +
|     | True  | False |        |
+     +-------+-------+        +
|     | False | True  |        |
+     +-------+-------+--------+
|     | True  | True  | True   |
+-----+-------+-------+--------+
| or  | False | False | False  |
+     +-------+-------+--------+
|     | True  | False | True   |
+     +-------+-------+        +
|     | False | True  |        |
+     +-------+-------+        +
|     | True  | True  |        |
+-----+-------+-------+--------+

----

.. _restruct-width:

列幅の変更
==================================================
- CSV テーブルとリストテーブルの列幅のデフォルトは等幅です。
- ``widths`` オプションを指定し、列幅を割合で指定できます。

.. code-block:: none

   .. csv-table::
      :widths: 1, 1, 2
   
      "A", "B", "A and B"
      "False", "False", "False"
      "True", "False", "False"
      "False", "True", "False"
      "True", "True", "True"
   
   .. list-table::
      :widths: 1,2,3
   
      * - A
        - B
        - A and B
      * - False
        - False
        - False
      * - True
        - False
        - False
      * - False
        - True
        - False
      * - True
        - True
        - True

.. csv-table::
   :widths: 1, 1, 2

   "A", "B", "A and B"
   "False", "False", "False"
   "True", "False", "False"
   "False", "True", "False"
   "True", "True", "True"

.. list-table::
   :widths: 1,2,3

   * - A
     - B
     - A and B
   * - False
     - False
     - False
   * - True
     - False
     - False
   * - False
     - True
     - False
   * - True
     - True
     - True

----

.. _restruct-table-header:

ヘッダーの指定
==================================================
グリッドテーブル
--------------------------------------------------
ヘッダーになる行の下に ``=`` で線を書きます。

.. code-block:: none

   +-------+-------+---------+
   | A     | B     | A and B |
   +=======+=======+=========+
   | False | False | False   |
   +-------+-------+---------+
   | True  | False | Flase   |
   +-------+-------+---------+
   | False | True  | False   |
   +-------+-------+---------+
   | True  | True  | True    |
   +-------+-------+---------+

+-------+-------+---------+
| A     | B     | A and B |
+=======+=======+=========+
| False | False | False   |
+-------+-------+---------+
| True  | False | Flase   |
+-------+-------+---------+
| False | True  | False   |
+-------+-------+---------+
| True  | True  | True    |
+-------+-------+---------+

グリッドテーブル
--------------------------------------------------
ヘッダーになる行の下に ``=`` で線を書きます。

.. code-block:: none

   ====== ====== =======
   A      B      A and B
   ====== ====== =======
   False  False  False
   True   False  False
   False  True   False
   True   True   True
   ====== ====== =======

====== ====== =======
A      B      A and B
====== ====== =======
False  False  False
True   False  False
False  True   False
True   True   True
====== ====== =======

CSV テーブル
--------------------------------------------------
``header-rows`` オプションでヘッダーになる行を指定します。

.. code-block:: none

   .. csv-table::
      :header-rows: 1
   
      "A", "B", "A and B"
      "False", "False", "False"
      "True", "False", "False"
      "False", "True", "False"
      "True", "True", "True"
.. csv-table::
   :header-rows: 1

   "A", "B", "A and B"
   "False", "False", "False"
   "True", "False", "False"
   "False", "True", "False"
   "True", "True", "True"

リストテーブル
--------------------------------------------------
``header-rows`` オプションでヘッダーになる行を指定します。

.. code-block:: none

   .. list-table::
      :header-rows: 1
   
      * - A
        - B
        - A and B
      * - False
        - False
        - False
      * - True
        - False
        - False
      * - False
        - True
        - False
      * - True
        - True
        - True

.. list-table::
   :header-rows: 1

   * - A
     - B
     - A and B
   * - False
     - False
     - False
   * - True
     - False
     - False
   * - False
     - True
     - False
   * - True
     - True
     - True

----

.. _restruct-table-title:

テーブル名の追加
==================================================
.. code-block:: none

   .. csv-table:: 論理積の結果
   
      "A", "B", "A and B"
      "False", "False", "False"
      "True", "False", "False"
      "False", "True", "False"
      "True", "True", "True"

   .. list-table:: 論理和の結果
   
      * - A
        - B
        - A or B
      * - False
        - False
        - False
      * - True
        - False
        - True
      * - False
        - True
        - True
      * - True
        - True
        - True

.. csv-table:: 論理積の結果

   "A", "B", "A and B"
   "False", "False", "False"
   "True", "False", "False"
   "False", "True", "False"
   "True", "True", "True"

.. list-table:: 論理和の結果

   * - A
     - B
     - A or B
   * - False
     - False
     - False
   * - True
     - False
     - True
   * - False
     - True
     - True
   * - True
     - True
     - True
