# PercentLayout

### Explicación de como implementar PercentLayout para redimensionar los elementos de las actividades, segun el tamaño de pantalla

* Copiar en el gradle lo siguiente:

    compile 'com.android.support:percent:25.0.0'

* Poner en el layout de la actividad en la que esten los elemtos que quieras redimensionar lo siguiente:

```html
<android.support.percent.PercentRelativeLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".NumericPadFragment">
```
* Cerrar el PercentLayout al final del layout
```html
    </android.support.percent.PercentRelativeLayout>
```    

* Para dar a cada elemento el porcentaje de pantalla deseado:
    ```html
    app:layout_widthPercent="33%"
    app:layout_heightPercent="25%"
    ````
* Hay que tener cuidado con los padding y con los margin, que tambien forman parte del porcentaje de pantalla.

### Ejemplo de un layout de una actividad con PercentilLayout
```html
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context="com.cazallau.calculator.NumericPadFragment">

    <android.support.percent.PercentRelativeLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".NumericPadFragment">

    <Button
        android:id="@+id/activity_main_number7"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:text="7"
        android:background="@drawable/border_number_pad_button"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number8"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:layout_toRightOf="@id/activity_main_number7"
        android:background="@drawable/border_number_pad_button"
        android:text="8"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number9"
        app:layout_widthPercent="34%"
        app:layout_heightPercent="25%"
        android:layout_toRightOf="@id/activity_main_number8"
        android:background="@drawable/border_number_pad_button"
        android:text="9"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number4"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number7"
        android:background="@drawable/border_number_pad_button"
        android:text="4"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number5"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number7"
        android:layout_toRightOf="@id/activity_main_number4"
        android:text="5"
        android:background="@drawable/border_number_pad_button"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number6"
        app:layout_widthPercent="34%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number7"
        android:layout_toRightOf="@id/activity_main_number5"
        android:background="@drawable/border_number_pad_button"
        android:text="6"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number1"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number4"
        android:background="@drawable/border_number_pad_button"
        android:text="1"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number2"
        app:layout_widthPercent="33%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number4"
        android:layout_toRightOf="@id/activity_main_number1"
        android:background="@drawable/border_number_pad_button"
        android:text="2"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number3"
        app:layout_widthPercent="34%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number4"
        android:layout_toRightOf="@id/activity_main_number2"
        android:background="@drawable/border_number_pad_button"
        android:text="3"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_number0"
        app:layout_widthPercent="50%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number1"
        android:background="@drawable/border_number_pad_button"
        android:text="0"
        android:textSize="25dp"/>

    <Button
        android:id="@+id/activity_main_comma"
        app:layout_widthPercent="50%"
        app:layout_heightPercent="25%"
        android:layout_below="@id/activity_main_number1"
        android:layout_toRightOf="@id/activity_main_number0"
        android:background="@drawable/border_number_pad_button"
        android:text="."
        android:textSize="25dp"/>

    </android.support.percent.PercentRelativeLayout>
    </RelativeLayout>
```