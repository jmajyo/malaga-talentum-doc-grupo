### Como utilizar los mapas en Android
 1. En el proyecto cambiar las opciones para que compile con un google API
 1. Hay que ir a google console developers y acceder una vez dentro buscar la API de los mapas para android, generar una clave y esa es la que añadiremos al paso 3 donde pone Your key API
 1. En el build.gradle hay que añadir compile  
 ```
 'com.google.android.gms:play-services-maps:10.0.1'
 ```
 1. En el Androidmanifest.xml hay que añadir este trozo de código dentro de la parte aplication
```xml
  <!-- Google Maps API Key -->
        <meta-data
            android:name="com.google.android.maps.v2.API_KEY"
            android:value="Your key API" />
        <meta-data
            android:name="com.google.android.gms.version"
            android:value="@integer/google_play_services_version" />
```
 5. En el Androidmanifest.xml hay que añadir estos permisos
 Estos permisos hay que añadirlos antes de las etiquetas aplication. OJO donde pone com.jmajyo.helloworldmaps hay 
 que poner tu paquete
 ```xml
 <permission
    android:name="com.jmajyo.helloworldmaps.permission.MAPS_RECEIVE"
    android:protectionLevel="signature" />
<uses-permission android:name="com.jmajyo.helloworldmaps.permission.MAPS_RECEIVE" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="com.google.android.providers.gsf.permission.READ_GSERVICES" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<!-- Required to show current location -->
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<!-- Required OpenGL ES 2.0. for Maps V2 -->
<uses-feature
    android:glEsVersion="0x00020000"
    android:required="true" />
```

6. Ahora ya estamos listo para añadir un mapa. Nos vamos al layout y ponemos un fragment.
```xml
 <fragment
        android:id="@+id/activity_map___map_fragment"
        android:name="com.google.android.gms.maps.MapFragment"
        android:layout_width="match_parent"
        android:layout_height="300dp"/>
```
## Importante ejecutar en un emulador/telefono que tenga las Googles APIS