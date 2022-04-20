```solidity []
interface Mintoooor {
    function mint(uint8 v, bytes32 r, bytes32 s) external payable;
}

contract Foo is Mintoooor {
    function mint(uint8 v, bytes32 r, bytes32 s) external payable override {
        address a = ecrecover(MAGIC, v, r, s);
        // mint to `a`
    }
}
```
