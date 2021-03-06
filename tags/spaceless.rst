``spaceless``
=============

*HTMLのタグとタグの間にある* 空白文字を除去するには、``spaceless`` タグを使います。
HTMLタグの中にある空白文字や、プレーンテキストの中の空白文字の除去には使いません:

.. code-block:: jinja

    {% spaceless %}
        <div>
            <strong>foo</strong>
        </div>
    {% endspaceless %}

    {# output will be <div><strong>foo</strong></div> #}

このタグは、生成されるHTMLコンテンツのサイズの "最適化" を意図したものではなく、
単に、特定の状況下で起こるブラウザのレンダリングの癖を回避するために、HTMLタグの間の空白文字を
取り除くことを意図するものです。

.. tip::

    生成されたHTMLのコンテンツサイズを最適化したい場合は、出力の gzip
    圧縮を代わりに使用してください。

.. tip::

    HTMLの文字列の中の余分な空白文字を、本当にすべて除去するようなタグを作成したいと
    したら、それは、思ったほど簡単でもないことに気づかされることでしょう
    (例えば、``textarea`` や ``pre`` タグのことを考えてみてください)。 Tidyなどのサードパーティの
    ライブラリを使う考えの方がよいかもしれません。

.. tip::

    空白文字のコントロールについての詳細については、ドキュメントの
    :doc:`このトピックの詳しい解説<../templates>` のセクションをご覧いただき、
    タグにおいて、空白文字コントロール修飾子 (whitespace control modifier) を使用する方法を学習してください。

.. 2012/08/08 goohib 75b954c1833274bb2e604675ce297484eb112db6
