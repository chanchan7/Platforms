Introduction
=====

.. _installation:

简要介绍
------------
    社会治理与风险防控共性基础平台，基于区块链底层基础设置，提供数字身份、智能合约、数字共享、隐私计算等多维度核心能力，向上打造区块链生态应用场景，助力社会治理与风险防控的高效协同监管。

.. To use Lumache, first install it using pip:

.. .. code-block:: console

..    (.venv) $ pip install lumache

核心价值
----------------
    提升社会治理与风险防控数据可信共享：实现各个系统原始数据或数据指纹上链流通，为参与方跨系统之间的数据共享提供可信能力基础。
    提升社会治理与风险防控效度：打破传统中心化平台社会治理模式，采用分布式多方共识、一主多链、智能合约等技术手段，全面提升社会治理效率、治理有效性。

.. To retrieve a list of random ingredients,
.. you can use the ``lumache.get_random_ingredients()`` function:

.. .. autofunction:: lumache.get_random_ingredients

.. The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
.. or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
.. will raise an exception.

.. .. autoexception:: lumache.InvalidKindError

.. For example:

.. >>> import lumache
.. >>> lumache.get_random_ingredients()
.. ['shells', 'gorgonzola', 'parsley']

