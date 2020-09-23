# Here maps (Android) package for React Native

## Install

```SH
yarn add react-native-here-maps-android
```

In AndroidManifest.xml add:

```XML
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```

In MainApplication.java:

```Java
import com.heremapsrn.react.map.HereMapPackage;

protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
          new MainReactPackage(),
          new HereMapPackage() // <------ Add this line
      );
    }
```

## Here Maps license
Go to [HERE website](https://developer.here.com/develop/mobile-sdks) and create your license key.


Then, open AndroidManifest.xml and update this section with your license.

```XML
    <!-- HEREMaps -->
    <meta-data
        android:name="com.here.android.maps.appid"
        android:value="YOUR-APP-ID-HERE" />

    <meta-data
        android:name="com.here.android.maps.apptoken"
        android:value="YOUR-APP-TOKEN-HERE" />

    <meta-data android:name="com.here.android.maps.license.key"
        android:value="YOUR-LICENSE-KEY-HERE"/>
```
