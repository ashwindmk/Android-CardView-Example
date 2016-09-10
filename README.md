# Android-CardView-Example
Shows card view for clickable list of movies

Create a simple recycle view and make the following changes:

Add cardview dependency
####app/build.gradle
```java
...
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    testCompile 'junit:junit:4.12'
    compile 'com.android.support:appcompat-v7:24.2.0'

    //cardview dependencies
    compile 'com.android.support:design:24.2.0'
    compile 'com.android.support:cardview-v7:24.2.0'
    compile 'com.android.support:recyclerview-v7:24.2.0'
}
```

Change the row layout using cardview widget
####movies_list_row.xml
```xml
<RelativeLayout...>
    ...
    <android.support.v7.widget.CardView
        android:id="@+id/card_view"
        android:layout_gravity="center"
        android:layout_width="fill_parent"
        android:layout_height="100dp"
        android:layout_margin="5dp"
        card_view:cardCornerRadius="2dp"
        card_view:contentPadding="10dp">

        <RelativeLayout
            android:layout_width="fill_parent"
            android:layout_height="fill_parent">

            <TextView
                android:id="@+id/title"
                android:textColor="#222222"
                android:textSize="16dp"
                android:textStyle="bold"
                android:layout_alignParentTop="true"
                android:layout_width="match_parent"
                android:layout_height="wrap_content" />

            <TextView
                android:id="@+id/genre"
                android:layout_below="@id/title"
                android:layout_width="match_parent"
                android:layout_height="wrap_content" />

            <TextView
                android:id="@+id/year"
                android:textColor="#999999"
                android:layout_width="wrap_content"
                android:layout_alignParentRight="true"
                android:layout_height="wrap_content" />

        </RelativeLayout>

    </android.support.v7.widget.CardView>
</RelativeLayout>
```
