``join``
========

``join`` フィルタは、シーケンスの要素を連結した文字列を
返します:

.. code-block:: jinja

    {{ [1, 2, 3]|join }}
    {# returns 123 #}

デフォルトでは、要素間のセパレータは空文字ですが、オプションの第1引数で、
これを定義することができます:

.. code-block:: jinja

    {{ [1, 2, 3]|join('|') }}
    {# returns 1|2|3 #}

.. 2012/08/09 goohib b096e21daa6647cd23063c3a4e4280ad81df8f84
