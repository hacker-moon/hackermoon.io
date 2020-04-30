### Brief

发起者：Web3 Foundation

赏金要求：Await InBlock Or Broadcast Status When Sending Extrinsic

截止日期：无

奖励金额：$490

申请链接：https://gitcoin.co/issue/scs/substrate-api-client/65/4268

---

### Description

(for v2.0.0-alpha.5 and later) The lifetime of an extrinsic goes like this:

```
send {"id":"3","jsonrpc":"2.0","method":"author_submitAndWatchExtrinsic","params":["0x2d0284d43593c715fdd31c61141abd04a99fd6822c8558854ccde39a5684e7a56da27d017693d988ff9b4d3577c0b9d2b9424e647fbec5875fef096644e311cb7499fd2a7cb99850c7e2806ffafecb3c63de17caa382340752077d6ca63e8995564f7d820068000400ce8f99245b836fa93f021c02c14a80d5029e2d43fb6265a0c610e5ac8d043e1b02286bee"]}
get {"jsonrpc":"2.0","result":232,"id":"3"}
get {"jsonrpc":"2.0","method":"author_extrinsicUpdate","params":{"result":"ready","subscription":232}}
get {"jsonrpc":"2.0","method":"author_extrinsicUpdate","params":{"result":{"broadcast":["QmfSF4VYWNqNf5KYHpDEdY8Rt1nPUgSkMweDkYzhSWirGY","Qmchhx9SRFeNvqjUK4ZVQ9jH4zhARFkutf9KhbbAmZWBLx","QmQJAqr98EF1X3YfjVKNwQUG9RryqX4Hv33RqGChbz3Ncg"]},"subscription":232}}
get {"jsonrpc":"2.0","method":"author_extrinsicUpdate","params":{"result":{"inBlock":"0x3104d362365ff5ddb61845e1de441b56c6722e94c1aee362f8aa8ba75bd7a3aa"},"subscription":232}}
get {"jsonrpc":"2.0","method":"author_extrinsicUpdate","params":{"result":{"finalized":"0x3104d362365ff5ddb61845e1de441b56c6722e94c1aee362f8aa8ba75bd7a3aa"},"subscription":232}}
```

currently, we only offer to submit and await `ready` or `finalized`. It would make sense to support `inBlock` too and maybe `broadcast`.
