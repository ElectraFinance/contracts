# Examples

```ts
// ethers V5
import { CFD__factory } from "@electra.finance/contracts/lib/ethers-v5";
import { ethers } from "ethers";

const provider = new ethers.providers.StaticJsonRpcProvider(
  "https://bsc-dataseed.binance.org/"
);
const cfdContractAddress = "0x1e2f9e10d02a6b8f8...";
const cfdContract = CFD__factory.connect(cfdContractAddress, provider);

cfdContract.depositAsset("0xe4ca1f75eca62");

const erc20Contract = ERC20__factory.connect(tokenAddress, provider);
```

```ts
// web3
import Web3 from "web3";
import { CFD } from "@electra.finance/contracts/lib/web3";
import CFDContractABI from "@electra.finance/contracts/abis/CFD.json";

const web3 = new Web3("https://bsc-dataseed.binance.org/");
const cfdContractAddress = "0x1e2f9e10d02a6b8f8...";

const cfdContract = new web3.eth.Contract(
  CFDContractABI,
  cfdContractAddress
) as unknown as CFD;

cfdContract.methods.depositAsset("0xe4ca1f75eca62");
```
