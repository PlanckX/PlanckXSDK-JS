# PlanckXSDK-JS

### Welcome to the PlanckX SDK！

The PlanckX SDK  contains  the basic SDK tools. You can match the PlanckX platform account with your game account, And link the NFT assets holder（Usually the player who bought the NFT） by the asset owner to the game for use.

### MetaMask

You need to install Metamask plugin

### In the Browser

Then import `lib` folder in your project. (jquery.min.js,web3.min.js,pxsdk.min.js)
and include `pxLib.min.js` in your html file.

````html
   <script type="text/javascript" src="pxLib.min.js" id="pxLib"></script>
````
### Usage
-  New
````javascript
    var pxsdk = new Pxsdk();
````
````
   Call the init method first and then the others.
````
### Interface
-  Init
````javascript
   /**
      * @param chainId:Number
      * @param callback:function.
      */
    pxsdk.init(chainId,callback)
````

- Get signature of account
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.sendSign(callback)
````

- Login
````javascript
   /**
     * @param access_key:String
     * @param address:String
     * @param nonce:String
     * @param signature:String.
     */
    pxsdk.login(access_key,address,nonce,signature,callback)
````

- Get all of the player's NFT
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.getNFTByPlayer(callback)
````

- Get all NFT's in the game
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.getNFTList(callback)
````

- Query NFT assets by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.getNFTByTokenId(tokenId, callback)
````

- Transfer NFT by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param toAddress:String
     * @param callback:function.
     */
    pxsdk.transferNFT(tokenId,toAddress,callback)
````

- Query NFT sell Approve by TokenIds
````javascript
   /**
     * @param tokenIds:Array<Number>
     * @param callback:function.
     */
    pxsdk.getApproveSellNFTBox(tokenIds,callback)
````

- Approve NFT sell by TokenIds
````javascript
   /**
     * @param tokenIds:Array<Number>
     * @param callback:function.
     */
    pxsdk.approveSellNFTBox(tokenIds,callback)
````

- Query Current TokenList for Sell Parameter
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.getCurrTokenList(callback)
````

- Sell NFT by tokenIds
````javascript
   /**
     * @param tokenIds:Array<Number>
     * @param tokenAddress:String
     * @param amounts:Array<Number>
     * @param callback:function.
     */
    pxsdk.sellNFTBox(tokenIds,tokenAddress,amounts,callback)
````

- Query NFT buy Approve by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.getApproveBuyNFTBox(boxId,callback)
````

- Approve NFT buy by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param isClear:Boolean
     * @param callback:function.
     */
    pxsdk.approveBuyNFTBox(boxId,isClear,callback)
````

- Buy NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.buyNFTBox(boxId,callback)
````

- Pull NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.pullNFTBox(boxId,callback)
````

- Query Selling BoxIds NFT
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.getSellingBoxIds(callback)
````

- Query Selling BoxIds NFT by Owner
````javascript
   /**
     * @param owner:String
     * @param callback:function.
     */
    pxsdk.getSellingBoxIdsOfOwner(owner,callback)
````

- Query Selling BoxId NFT by TokenId
````javascript
   /**
     * @param TokenId:String
     * @param callback:function.
     */
    pxsdk.getSellingBoxIdOfTokenId(TokenId,callback)
````

- Query NFTContractAddress NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.getNFTContractBox(boxId,callback)
````

- Query Owner NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.getOwnerBox(boxId,callback)
````

- Query TokenIds NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.getTokenIdsBox(boxId,callback)
````

- Query TokenAddress NFT by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.getTokenAddressBox(boxId,callback)
````

- Query Approve by TokenAddress
````javascript
   /**
     * @param tokenAddress:String
     * @param amount:Number
     * @param callback:function.
     */
    pxsdk.getApproveOrderBox(tokenAddress,amount,callback)
````

- Approve TokenAddress
````javascript
   /**
     * @param tokenAddress:String
     * @param amount:Number
     * @param isClear:Boolean
     * @param callback:function.
     */
    pxsdk.approveOrderBox(tokenAddress,amount,isClear,callback)
````

- Order by BoxId
````javascript
   /**
     * @param boxId:Number
     * @param callback:function.
     */
    pxsdk.setOrderBox(boxId,tokenAddress,amount,callback)
````
