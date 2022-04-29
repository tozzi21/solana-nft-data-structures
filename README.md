# do119-solana-nft-experimentation

sequence of steps
1. upload Image to Arweave
2. create NFT JSON metadata
3. set image URL to Arweave
4. upload NFT JSON to Arweave
5. mint NFT with URL to NFT on Arweave

Tools:
===
Upload with https://app.ardrive.io/

Mint
===
use Metaboss release from GitHub:

./metaboss-ubuntu-latest mint one --keypair /home/thorsten/.config/solana/id.json --receiver 6iSbmKmN1W86U82PYc36AzpN7A92ZGRiAKctpQ2Zt9SU --external-metadata-uri https://ujl274motwoo4qi5lko3zbfdyvkkv3h4qemymqlkhj2at6xlldda.arweave.net/olev8Y6dnO5BHVqdvISjxVSq7PyBGYZBajp0CfrrWMY -l debug

Notes:
* Creator remains update authority over NFTs printed from Master Edition, even when transferred to other owners wallet
* When NFT is set as immutable, it can not be updated anymore.
* When NFT is printed from Master Edition, but Master Edition was not immutable, then printed NFT is not immutable
* If Master Edition is changed to immutable, but printed NFT is already in another persons wallet, it can still be modified

Notes2:
* Do not use or set --immutable
* We can set --primary-sale-happened
* Use --receiver if different to creator

Update Name
===
./metaboss-ubuntu-latest update name --keypair /home/thorsten/.config/solana/id.json --account 8RYXjuazzrgYkdpRBVSVdxKKkD5H4oD6EzC9RcmfFjsa --new-name DO119LaunchPad -l debug

Update URI
===
./metaboss-ubuntu-latest update uri --keypair /home/thorsten/.config/solana/id.json --account 8RYXjuazz
rgYkdpRBVSVdxKKkD5H4oD6EzC9RcmfFjsa --new-uri https://arweave.net/vA4uXyaHBa2kOJRrO6Stqppy326BgK-0No4P63KROmM -l debug

Signing
===
./metaboss-ubuntu-latest sign one --keypair /home/thorsten/.config/solana/id.json --account 5copHM2D89Z9D7MD6JRDNwqkcVXcVGwxSNCZup7V1Jnn
Tx sig: 2fkr55NPoZvn14EouKpBo6P3qzPAJJQ3M9zdTFRzKGZiiJ2cLCTtgB5kiHjHsqsWuyvYBywWVT8ZGscwkasSVrKX



