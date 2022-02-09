# klaynNFT_pinanta
피나타를 사용하여 KIP17발행

사용법

사전작업
.env파일 생성하여 pinata API키, 시크릿, JWT등을 넣고, PRIVATE_KEY에는 지갑 개인키를 넣는다.     
프로젝트에 NFT파일을 위치시킨다.

1. uploadFilse.js에서 14번째줄 주석 해제, 15줄 주석처리 후 node uploadFile.js

2. 이후 터미널창의 ipfsHash라고 나온값을 meta.json의 image에 CID라고 적힌 부분에 붙여넣기

3. upLoadFiles.js가 수정되었다면 한번더 node uploadFile.js
   이후 나온 ipfsHash를 잘 저장
   
4. 컴파일 및 마이그레이션: truffle migrate --compile-all --network babbab

5. 트러플콘솔진입: truffle console --network babob

6. 트러플 콘솔창에서
   nft = await MyNFTs.deployed()
   nft.mint("http://gateway.pinata.cloud/ipfs/ipfsHash")
