分布式数字身份模块  
==================================




1. API列表

- :ref:`注册DID账户`
- :ref:`DID账户吊销`
- :ref:`创建DID文档`
- :ref:`查询DID文档`

2. API详情


.. _注册DID账户:

注册DID账户

``Request<TxHashResponse> register(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcRegisterReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction`` - 账户注册的交易体.
-  ``nodeIds`` - 请求向这些节点发送.


.. _did账户吊销:

DID账户吊销

``Request<TxHashResponse> destroy(Transaction transaction, int... nodeIds);``
``Request<ReceiptResponse> grpcDestroyReturnReceipt(Transaction transaction, int... nodeIds);``

参数：

-  ``transaction`` -  DID账户吊销的交易体.
-  ``nodeIds`` -  请求向这些节点发送.

.. _创建did文档:

创建DID文档

``public DIDDocument(String didAddress, string publicKey, String[] admins);``

参数：

-  ``didAddress``: ``string`` -  DID账户地址
-  ``publicKey``: ``string``  -  DID账户公钥
-  ``admins``: ``string[]`` -  写入多条监管信息

.. _查询did文档:

查询DID文档

``Request<DIDDocumentResponose> getDIDDocument(String didAddress, int... nodeIds);``

参数：

-  ``didAddress``: ``string`` -  DID账户地址
-  ``nodeIds``: ``int`` -  请求向这些节点发送

