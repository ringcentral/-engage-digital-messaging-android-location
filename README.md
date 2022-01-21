Engage Digital Messaging Maps SDK for Android
=============================================

Engage Digital Messaging Maps SDK for Android is a plug-in for the [Engage Digital Messaging Android SDK](https://github.com/ringcentral/engage-digital-messaging-android).
It allows your users to send location messages through you Engage Digital Messaging channel using Google APIs.

Supported Versions
------------------

The Engage Digital Messaging Maps SDK for Android is currently supporting **Android 5.0 (API 21) and above** and is only compatible with the [Engage Digital Messaging Android SDK](https://github.com/ringcentral/engage-digital-messaging-android/blob/master/CHANGELOG.md) **version 2.3.0 and above**.

Please note that the Engage Digital Messaging Maps SDK for Android will require the usage of [AndroidX](https://developer.android.com/jetpack/androidx)

Getting Started
---------------

Before going through any of the following step please make sure that you have a working implementation of the [Engage Digital Messaging Android SDK](https://github.com/ringcentral/engage-digital-messaging-android).

Follow these steps to install/initialize the Engage Digital Messaging Maps SDK for Android:
1. [Installation using gradle](#install-the-engage-digital-messaging-maps-sdk-for-android-using-gradle)
2. [Google API keys](#api-keys)
3. [Initialize the Engage Digital Messaging Maps SDK](#engage-digital-messaging-maps-initialization)
4. [Customize the Engage Digital Messaging Maps SDK appearance](#customizing-the-engage-digital-messaging-maps-sdk-ppearance)

Install the Engage Digital Messaging Maps SDK for Android using Gradle
----------------------------------------------------------------------

Add these to your Grade file:
### Repositories
```java
repositories {
    maven {
        url "https://raw.github.com/ringcentral/engage-digital-messaging-android-location/master"
    }
}
```

### Dependencies
```java
dependencies {
    implementation 'com.ringcentral.edmessagingmapssdk:edmessagingmapssdk:1.0.0'
}
```

API keys
--------

The Engage Digital Messaging Maps SDK for Android takes advantage of the Google APIs to provide maps capabilities to the Engage Digital Messaging Android SDK and thus requires the usage of Google API keys.

| Key | Restriction(s) | Purpose(s) |
| --- | -------------- | ---------- |
| [Android key](#android-key) | [Maps SDK for Android](https://developers.google.com/maps/documentation/android-sdk/overview) | Used to display the map. |
| [Maps key](#maps-key) | [Places API](https://developers.google.com/maps/documentation/places/web-service/overview) | Used to enable the address search. |

Engage Digital Messaging Maps initialization
--------------------------------------------

1. Add your Android key (see [API keys](#api-keys)) to your application's manifest (please bear in mind that the Engage Digital Messaging Android SDK won't show the location button if this API key is not present):
```xml
<application
  <meta-data android:name="com.google.android.geo.API_KEY" android:value="YOUR_API_KEY" />
</application>
```


2. Initialize the `EngageDigitalMessagingMaps` singleton instance:
```java
EngageDigitalMessagingMaps engageDigitalMessagingMaps = EngageDigitalMessagingMaps.getInstance();
```

3. (OPTIONAL) Set your [Maps key](#api-keys) (the search button won't be displayed if this API key is not present):
```java
engageDigitalMessagingMaps.setMapsApiKey("YOUR_MAPS_KEY");
```

4. Override the `onLocationButtonClick` on your `DimeloListener`:
```java
Dimelo dimelo = Dimelo.getInstance();
Dimelo.DimeloListener dimeloListener = new Dimelo.DimeloListener() {
    ...
    @Override
    public void onLocationButtonClick(Chat chat) {
        super.onLocationButtonClick(chat);
        engageDigitalMessagingMaps.build(MainActivity.this);
        engageDigitalMessagingMaps.setMapsListener(new EngageDigitalMessagingMaps.EngageDigitalMessagingMapsListener() {
            @Override
            public void sendLocationMessage(Intent data) {
                super.sendLocationMessage(data);
                Dimelo.getInstance().sendLocationMessage(data, chat);
            }
        });
    }
};
```

Customizing the Engage Digital Messaging Maps SDK Appearance
------------------------------------------------------------

[See how to customize the Engage Digital Messaging Maps SDK appearance using the Android Resource folders](Customization.md).
