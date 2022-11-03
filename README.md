# Tokencat
Tokencat is a tool that uses symbolic execution techniques to detect erc20 authentication vulnerabilities.

# Paper
You can find our paper about the design, implementation, and experimental results of Tokencat at [paper link](https://github.com/hzysvilla/TokenCat/raw/main/TokenCat_paper.pdf) or https://ieeexplore.ieee.org/document/9839252.

> In this work, we detect the authentication implementation of the flaws in ERC20 token, which has not been done before. We find the authentication process of the token is implemented by operating the authentication data structure of the token. Therefore, we capture the operations of the authentication data structure in token contract to infer authentication behaviors and detect authentication defects. However, it’s not a simple task as most smart contracts are not open source and the bytecode of token contract lacks type information. To tackle these problems, we utilize symbolic execution on the token bytecode, then identify the authentication data structure and capture the operations by parsing the symbolic expressions, and finally detect authentication defects through the inferred authentication behavior. To best our knowledge, this is the first work to detect the flaws in the implementation of authentication in ERC20 Token. To automate the analysis, we implement our approach in a new tool named TokenCat and use it to inspect 245,822 tokens. As a result, the TokenCat found 491 ERC20 token authentication implementation flaws with 94% precision.

# Citing in Academic Work

Welcome to cite our paper:
```shell
@INPROCEEDINGS{9839252,
author={He, Zheyuan and Liao, Zhou and Luo, Feng and Liu, Dijun and Chen, Ting and Li, Zihao},
booktitle={ICC 2022 - IEEE International Conference on Communications}, 
title={TokenCat: Detect Flaw of Authentication on ERC20 Tokens}, 
year={2022},
pages={4999-5004},
doi={10.1109/ICC45855.2022.9839252}}
```

# The Catalog of TokenCat 

## source code
The source code is in Tokencat_source_code and the core source code is in the Tokencat_source_code/mythril/analysis/module/modules/ApproveCheck.py

## experiment result
 * `Inconsistent Authentication.xls`：token’s address list with inconsistent authentication
 * `Token authorized transfer.xls`：token’s address list with token authorized transfer
 * `Unlimited Authorization.xls `：token’s address list with unlimited Authorization
 * `Unreasonable Approval Authorization.xls`：token’s address list with unreasonable Approval Authorization
 
 
# Contact us
If you have any problems in using our tool, please send emails to ecjgvmhc@gmail.com
