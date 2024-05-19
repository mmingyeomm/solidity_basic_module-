# Solidity 컨트랙트 작성 및 배포 가이드 (Remix 사용)

이 문서는 Remix IDE를 사용하여 Solidity로 스마트 컨트랙트를 작성하고 이더리움 네트워크에 배포하는 과정을 안내합니다.

## 준비사항

- MetaMask 설치 및 설정
- Remix IDE에 접속: [https://remix.ethereum.org](https://remix.ethereum.org)

## 1. 스마트 컨트랙트 작성

### 1.1. Remix IDE 접속 및 파일 생성

1. Remix IDE에 접속합니다.
2. 좌측 파일 탐색기에서 `contracts` 폴더를 선택한 후, `New File` 버튼을 클릭하여 `MyContract.sol` 파일을 생성합니다.

### 1.2. MyContract.sol 작성

`MyContract.sol` 파일에 다음 코드를 작성합니다:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract MyContract {
    string public message;

    constructor(string memory initMessage) {
        message = initMessage;
    }

    function updateMessage(string memory newMessage) public {
        message = newMessage;
    }
}
