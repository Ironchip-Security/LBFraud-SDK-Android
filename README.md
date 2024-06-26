# LBFraud-SDK-Android

## Setup

### Supported versions
| Platform | Supported versions |
| --- | --- |
| Android | 5.0.0+ |
    
<br>

### Add Ironchip Location Based Fraud SDK

<br>

#### Add our library in other projects

First, on the *setting.gradle* file, reference the remote repository where the library is located. 
``` gradle
dependencyResolutionManagement {
    ...

    repositories {
        maven { url 'https://jitpack.io' }
        ...
    }
}
```

Then, inside the *gradle.build* file, add the dependency to the sdk.
``` gradle

dependencies {
    ...
    implementation 'com.github.Ironchip-Security:LBFraud-SDK-Android:1.2.13'
    ...
}

```

### Permissions
This library require the permissions:

``` xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />

<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
<uses-permission android:name="android.permission.CHANGE_WIFI_STATE" />

<uses-permission android:name="android.permission.INTERNET" />
```


## Usage

To make full use of the potential of the sdk, the ACCESS_FINE_LOCATION permission needs to be granted.

[How to request permissions](https://developer.android.com/training/permissions/requesting)

```java
import com.ironchip.ironchiplbfraudandroidsdk.LBFraudSDK;
...

// Replace APIKEY with the desired generated api key.
LBFraudSDK fraud = new LBFraudSDK(this, "APIKEY");
// By default our SDK target to the production environment.
// In case you desire to target a diferent enviroment:
// LBFraudSDK fraud = new LBFraudSDK(this, "APIKEY", Environment.Testing);

//public enum Environment {
//    Production,
//    Testing,
//    Development
//}

String transactionID = "random_identifier_generated"; // Transaction identifier request for fraud results
String userID = "john.doe@gmail.com"; // User identifier

Map<String, Object> extraData = new HashMap<>(); // Extra information for analysis
extraData.put("concept", "Book august");
extraData.put("amount", new Integer(30));
extraData.put("operation", "booking");

// TransactionID (required,unique): transaction identifier request for fraud results
// UserID (required): User identifier
// ExtraData (optional): extra information for analysis
// The sendTransaction can be provided with 2 callbacks, one is executed when the transaction is finished
// and the other one is called in case an error did occure during the transaction process.
fraud.sendTransaction(transactionID, userID, extraData, () -> {
        // Add here any code you want to be executed after the transaction
        // has finished.
    }, exception -> {
        // Add here any code you want to perform in case of an error
        // during the transaction.
        // exception.printStackTrace()
});
```
