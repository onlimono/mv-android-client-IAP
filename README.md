## What is the MV Android Client with In-app Purchase

The MV Android Client with IAP is a runtime client which supports IAP services for the [Android&trade; operating system](https://www.android.com) intended to play games created with the [RPG Maker MV](http://www.rpgmakerweb.com) game development tool-kit.

There are a lot of marketing advantages to distribute demo games before distributing paid games on the Android system. This client can provide demo version and full version simultaneously by supporting In-app Purchase.

I just integrated [MV Android Client](https://github.com/AltimitSystems/mv-android-client) and [Android In-app Billing Version 3](https://github.com/anjlab/android-inapp-billing-v3).

## Tutorial & Usage Support

The basic tutorial for MV Android Client is hosted at HBGames.org at the following URL:
[hbgames.org/forums/viewtopic.php?f=48&t=79391](http://www.hbgames.org/forums/viewtopic.php?f=48&t=79391)

Usage support is provided with this tutorial.

You just follow the provided tutorial after downloading this git files.

## IAP setting

In addition, you only need to modify two parts of the WebPlayerActivity.java file to implement the IAP services.

1) private static final String PRODUCT_ID = "SKU";
-> SKU needs to be modified with your product ID which can be set in Google Play Console.

2) bp = BillingProcessor.newBillingProcessor(this, "LICENSE_KEY", this);
-> LICENSE_KEY needs to be modified with RSA public key which is provided by Google Play Console.

## IAP implementation in RPG Maker MV

Now you can use two functions in RPG Maker MV.

1) window.IAP.purchaseGame()
-> You can launch the IAP's purchase window by running the function.

2) window.IAP.purchased()
-> The function returns true if in-app is purchased.

## License

The MV Android Client with In-app Purchase is under the [Apache License 2.0].

## Terms of Use

Free to use as long as credit is given to onlimono.
