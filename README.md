# PlanckXSDK-JS

### Welcome to the PlanckX SDK！

The PlanckX SDK  contains  the basic SDK tools. You can match the PlanckX platform account with your game account, And link the NFT assets holder（Usually the player who bought the NFT） by the asset owner to the game for use.

### Matemask

You need to install Matemask plugin

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

- Query NFT buy Approve by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.getApproveBuyNFT(tokenId,callback)
````

- Approve NFT buy by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param isClear:Boolean
     * @param callback:function.
     */
    pxsdk.approveBuyNFT(tokenId,isClear,callback)
````

- Buy NFT by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.buyNFT(tokenId,callback)
````

- Query NFT sell Approve by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.getApproveSellNFT(tokenId,callback)
````

- Approve NFT sell by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.approveSellNFT(tokenId,callback)
````

- Query Current TokenList for Sell Parameter
````javascript
   /**
     * @param callback:function.
     */
    pxsdk.getCurrTokenList(callback)
````

- Sell NFT by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param tokenAddress:String
     * @param amount:Number
     * @param callback:function.
     */
    pxsdk.sellNFT(tokenId,tokenAddress,amount,callback)
````

- Pull NFT by TokenId
````javascript
   /**
     * @param tokenId:Number
     * @param callback:function.
     */
    pxsdk.pullNFT(tokenId,callback)
````

