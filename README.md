
# AppCoins SDK Unity package

## Description

Streamline the process of adding Appcoins SDK to your Unity app through importing from the Unity Package Manager. Below you can see the video about how to integrate the SDK and after it a detailed installation guide of the same process.

<!---               
## Video

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/m-EZxdb7sUY/0.jpg)](https://www.youtube.com/watch?v=m-EZxdb7sUY)
-->
## Installation Guide

### Step 1 - Import Package
* Start by opening on the top menu bar the Window > Package Manager
* In the new window on the top left corner click on the + sign and select Import via git URL and paste the following link: [https://github.com/Aptoide/appcoins-sdk-unity-package](https://github.com/Catappult/appcoins-sdk-unity-package)
 * Wait to import and compile all files

### Step 2 - Add AptoPurchaseManager to the Main Camera game object + Set Params
* Select the Game Object, on the Inspector panel scroll to bottom
 * Add Component, search for AptoPurchaseManager
* Set the params of KEY, SKU (string divided by ";")** and Developer Payload 

### Step 3 - Setup the Purchase Button 
* Select the Play button, on the Inspector panel scroll to bottom
* Add entry on the OnClick area
* Drag and drop the Main Camera to the box under Runtime (on OnClick section) 
* After that select the Script AptoPurchaseManager and the method StartPurchase , to which you can set the sku**

### Step 4 - Setup the Consume Item Button
* Select the Consume button and in the inspector on the bottom add on the on click a new entry 
* Drag and drop the Main Camera to the box under Runtime (on OnClick section) 
* After that select the Script AptoPurchaseManager and the method ConsumeItem **

### Step 5 - Setup Manifest File
* Open the Manifest file (or create one in your Assets folder) and update the package name to your project 
* Set as well the queries and permissions

### Step 6 - Setup Build Graddle
* Add the implementation to import sdk

### Step 7 - Add OverrideExample and AppCoinsAdapter
* Update as well on the OverrideExample the line 1 package name and the line 27 on the getSharedPreferences
* Add the following file AppCoinsAdapter to access the AppCoins SDK

After that you can run and you have successfully integrate the Appcoins SDK on your Unity App through Package Manager.


** ADDITIONAL NOTES
This is a demo project to test integration, you should perform consumption after purchase of the item
The SKUs can be set on the AptoPurchaseManager SKU (Inspector of MainCamera - Game Object) or through AptoPurchaseManager Script accessing your backend and setting the string
You also can dinamically atribute the SKU para of the button and pass the SKU once calling the StartPurchase


