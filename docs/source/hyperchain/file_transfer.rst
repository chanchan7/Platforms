区块链传输模块

============

1. API列表

- :ref:`FileUpload`
- :ref:`FileDownload`
- :ref:`FileUpdate`

2. API详情


.. _FileUpload:

⽂件上传

参数：

-  ``filePath``: ``<path>`` - 文件路径.
-  ``description``: ``string`` - 文件描述信息.
-  ``userList``: ``string[]`` - ⽤户⽩名单.
-  ``nodeIdList``: ``int[]`` - 节点⽩名单.
-  ``pushNodes``: ``int[]`` - 上传节点.
-  ``accountJson``: ``string`` - 账户.
-  ``password``: ``string`` - 账户密码.

返回值

1. ``fileHash``: ``string`` - 文件哈希.
2. ``err``: ``err`` - 错误信息.

.. _FileDownload:

⽂件下载

参数：

-  ``tarPath``: ``<path>`` - tarPath有两种使⽤：1.传有效⽬录，会在给路径下以hash作为⽂件名保存⽂件；2.传有效⽂件路径,对该⽂件进⾏断点续传.
-  ``hash``: ``string`` - 文件哈希.
-  ``owner``: ``string`` - 文件持有者.
-  ``nodeID``: ``int`` - 表示发送下载请求的节点ID.
-  ``accountJson``: ``string`` - 账户.
-  ``password``: ``string`` - 账户密码.

返回值

1. ``filePath``: ``string`` - 文件下载路径.
2. ``err``: ``err`` - 错误信息.

.. _FileUpdate:

⽂件下载

参数：

-  ``fileUpdateTX``: ``<FileExtra>`` - 交易体

.. _FileExtra:

``FileExtra``成员包括：

-  ``hash``: ``string`` - 文件哈希.
-  ``fileName``: ``string`` - 文件名.
-  ``fileSize``: ``int64`` - 文件大小.
-  ``updateTime``: ``string`` - 修改时间.
-  ``nodeList``: ``string[]`` - 节点列表.
-  ``userList``: ``string[]`` - 用户列表.
-  ``fileDescription``: ``string`` - 文件描述.


返回值

2. ``err``: ``err`` - 错误信息.