# Como solucionar el fallo de la limitación de los 64k de metodos.

1. Para provocar el fallo basta con añadir la librería de google de play services, esta librería hay que añadirla en el
gradle

    `compile 'com.google.android.gms:play-services:10.0.1'`
1. Para solucionar el fallo, tenemos que añadir al gradle la librería de multidex que es la encargada de 
solucionar el fallo. Para ello añadimos la siguiente librería en el gradle  `compile 'com.android.support:multidex:1.0.1'` 
también hay que poner dentro del gradle en la parte de default configuration
`multiDexEnabled true`
```java
android {
    compileSdkVersion 25
    buildToolsVersion "25.0.2"
    defaultConfig {
        applicationId "com.jmajyo.multidexbigapplication"
        minSdkVersion 14
        targetSdkVersion 25
        versionCode 1
        versionName "1.0"
        testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"
        multiDexEnabled true
    }
```
3. Una vez hecho esto tenemos que crearnos una clase java que extienda de MultiDexApplication.

    Así quedaría la clase que acabamos de crear.
```java
package com.jmajyo.multidexbigapplication;

import android.support.multidex.MultiDexApplication;

public class MultidexBigApp extends MultiDexApplication{

}
```

4. Ahora ya solo queda indicarle al Androidmanifest que va a usar esta clase aplicación. Eso se hace con 
la siguiente línea `android:name=".MultidexBigApp"` 

    Con lo que el Androidmanifest quedaría así:
```java
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.jmajyo.multidexbigapplication">

    <application
        android:name=".MultidexBigApp"
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```
