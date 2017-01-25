### Para hacer un menu en Android

1. Se hace una nueva carpeta llamada menu dentro de res
1. Dentro de esta carpeta se pone el .xml del menú

![](pictures/menu.png)

```xml
<?xml version="1.0" encoding="utf-8"?>
<menu
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto">
    <item
        android:title="Add"
        android:id="@+id/menu_main_action_add_city"
        android:icon="@android:drawable/ic_menu_add"
        app:showAsAction="always" />
</menu>
```
Ej: Código de ejemplo para un menu con el icono del más.

3. En la actividad que se quiera el menu hay que sobre-escribir dos métodos.
```java
@Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu_main, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        int id = item.getItemId();

        if (id == R.id.menu_main_action_add_city) {

            Intent i = new Intent(CityListActivity.this, CityEditActivity.class);
            startActivity(i);

            return true;
        }

        return super.onOptionsItemSelected(item);
    }


```

Con este código ya se vería el menu y al pulsar el más llamaría a la actividad CityEditActivity.


### Bases de datos Realm

Para poder guardar en la base de datos por ejemplo la clase city debe extender de RealmObject
