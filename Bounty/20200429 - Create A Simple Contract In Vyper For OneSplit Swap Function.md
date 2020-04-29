
### Brief

项目名称：gonchs

截止日期：5月13日

奖励金额：$20

申请链接：https://gitcoin.co/issue/gonchs/gsapps/3/4259

---

### Requirements

Modify the following contract to make it work: https://gist.github.com/gonchs/8e3283f63a4305a13163c01e4e618b38

### Deliverable

Deployed and verified contract on Mainnet and an example transaction which calls swap function on our contract which then calls `swap` on [OneSplit contract](https://etherscan.io/address/0xc586bef4a0992c495cf22e1aeee4e446cecdee0e).

The transaction should make an actual swap of ERC20 tokens from DAI to BAT. Feel free to use any amount for testing. It could be just $0.001 if it passes.

### Existing work

I tried deploying this contract and calling the swap function which passes but it doesn't exchange any funds which suggest that `OneSplit#swap` may not even be called. Perhaps the interface definition is wrong?

Notes

Note that you will need the newest build of Vyper to compile this contract because it uses a `swap` as a function name which has been removed from the list of reserved keywords in the recent [commit](https://github.com/vyperlang/vyper/commit/d576b2f5bb5cdaa1128ada1077fb45e36b954996).

You can use the latest version of Vyper by cloning the git repo, running `docker build` from the root and then using it to compile the contract like this:

`docker run -v $(pwd):/code your-newly-built-vyper-image -f bytecode our_contract.vy`

Or if you want to replicate my exact environment, the version of Vyper I'm using is on commit [0671b7b](https://github.com/vyperlang/vyper/commit/0671b7b) but with "swap" keyword removed.
