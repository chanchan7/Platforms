区块链传输模块
==================================


文件传输
-------------------------
⽂件上传
~~~~~~~~~~~~~~~~~~~~~
``func (rpc *RPC) FileUpload(filePath string, description string, userList []string, nodeIdList []int, pushNodes []int, accountJson string, password string) (string, StdError)``

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
~~~~~~~~~~~~~~~~~~~~~
``func (rpc *RPC) FileDownload(tarPath, hash, owner string, nodeID int, accountJson string, password string) (string, StdError)``

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

⽂件更新
~~~~~~~~~~~~~~~~~~~~~
``func (rpc *RPC) FileUpdate(fileUpdateTX FileExtra) (StdError)``

参数：

-  ``fileUpdateTX``: ``<FileExtra>`` - 交易体

.. _FileExtra:

FileExtra成员包括：

-  ``hash``: ``string`` - 文件哈希.
-  ``fileName``: ``string`` - 文件名.
-  ``fileSize``: ``int64`` - 文件大小.
-  ``updateTime``: ``string`` - 修改时间.
-  ``nodeList``: ``string[]`` - 节点列表.
-  ``userList``: ``string[]`` - 用户列表.
-  ``fileDescription``: ``string`` - 文件描述.


返回值

1. ``err``: ``err`` - 错误信息.

交易处理
---------------------

.. _SignAndSendTx:

同步发送交易
~~~~~~~~~~~~~~~~~~~~~
``func (rpc *RPC) SignAndSendTx(transaction *Transaction, key interface{}) (*TxReceipt, StdError)``

参数：

-  ``transaction``: ``<Transaction>`` - 交易体
-  ``key``: ``<Key>`` - 交易发送⽅key.

返回值

1. ``txReceipt``: ``<TxReceipt>`` - 交易回执.
2. ``err``: ``err`` - 错误信息.

.. _GetTxByBlkNumAndIdx:

同步发送交易
~~~~~~~~~~~~~~~~~~~~~
``func (rpc *RPC) GetTxByBlkNumAndIdx(blkNum, index uint64) (*TransactionInfo, StdError)``

参数：

-  ``blkNum``: ``int`` - 区块号
-  ``index``: ``int`` - 交易在当前区块内的序号.

返回值

1. ``TransactionInfo``: ``<TransactionInfo>`` - 交易信息.
2. ``err``: ``err`` - 错误信息.