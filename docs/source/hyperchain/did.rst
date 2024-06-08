分布式数字身份模块  
==================================


分布式数字身份管理
-------------------------

.. _分布式数字身份建立:

分布式数字身份建立
~~~~~~~~~~~~~~~~~~~~~

``Request<TxHashResponse> register(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcRegisterReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction``: ``string`` -  分布式数字身份建立的交易体.
-  ``nodeIds``: ``int`` -  请求向这些节点发送.

返回值

1. ``didAddress``: ``string`` -  分布式数字身份.
2. ``err``: ``err`` - 错误信息.

.. _分布式数字身份存储:

分布式数字身份存储
~~~~~~~~~~~~~~~~~~~~~

``Request<TxHashResponse> storage(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcStorageReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction``: ``string`` -  分布式数字身份存储的交易体.
-  ``nodeIds``: ``int`` -  向这些节点存储分布式数字身份.

返回值

1. ``Success``: ``string`` -  存储成功信息.
2. ``err``: ``err`` - 错误信息.

.. _分布式数字身份查询:

分布式数字身份查询
~~~~~~~~~~~~~~~~~~~~~

``Request<TxHashResponse> getDid(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcGetDidReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction``: ``string`` -  分布式数字身份查询的交易体.
-  ``nodeIds``: ``int`` -  向这些节点查询分布式数字身份.

返回值

1. ``didAddress``: ``string`` -  分布式数字身份查询成功信息.
2. ``err``: ``err`` - 错误信息.

.. _分布式数字身份吊销:

分布式数字身份吊销
~~~~~~~~~~~~~~~~~~~~~

``Request<TxHashResponse> destroy(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcDestroyReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction``: ``string`` -  账户注册的交易体.
-  ``nodeIds``: ``int`` -  请求向这些节点发送.

返回值

1. ``err``: ``err`` - 吊销失败信息.

分布式数字身份监管信息管理
-------------------------
.. _分布式数字身份监管信息编辑:

分布式数字身份监管信息编辑
~~~~~~~~~~~~~~~~~~~~~

``public DIDDocument(String didAddress, string publicKey, String[] admins);``

参数：

-  ``didAddress``: ``string`` -  DID账户地址
-  ``publicKey``: ``string``  -  DID账户公钥
-  ``admins``: ``string[]`` -  写入多条监管信息

返回值

1. ``Success``: ``string`` -  写入成功信息.
2. ``err``: ``err`` - 错误信息.

.. _分布式数字身份监管信息查询:

分布式数字身份监管信息查询
~~~~~~~~~~~~~~~~~~~~~

``Request<DIDDocumentResponose> getDIDDocument(String didAddress, int... nodeIds);``

参数：

-  ``didAddress``: ``string`` -  DID账户地址
-  ``nodeIds``: ``int`` -  请求向这些节点发送

返回值

1. ``admins``: ``string[]`` -  监管信息.
2. ``err``: ``err`` - 错误信息.
