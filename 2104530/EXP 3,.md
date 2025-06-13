
# EXPERIMENT NO. 3

## Title: Android User Interface Design – Studying XML Files Required for UI Design


## 1. `AndroidManifest.xml`

This is one of the most critical files in an Android project. It provides essential information about your app to the Android system, which the system must have before it can run any of the app's code.

### **Key Responsibilities:**
- Declares activities, services, broadcast receivers, and content providers.
- Specifies required permissions (e.g., internet access).
- Declares the minimum and target SDK versions.
- Sets the launcher activity.
- Registers app-wide themes, icons, and more.

### **Example:**
```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.myapp">

    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
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

---

## 2. `activity_main.xml`

This is the layout file that defines the user interface for an Activity — typically the main screen.

### **Key Elements:**
- Defines the structure of UI using containers like `ConstraintLayout`, `LinearLayout`, etc.
- Includes UI widgets like `TextView`, `Button`, `EditText`, etc.
- Uses layout attributes to define position and size.

### **Example:**
```xml
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/welcome_message"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/button_text"
        app:layout_constraintTop_toBottomOf="@id/textView"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

---

## 3. `colors.xml`

This file defines color resources used in the app. Defining colors centrally ensures consistency and simplifies theme changes across the app.

### **Use Cases:**
- Primary and secondary theme colors
- Background, text, accent colors

### **Example:**
```xml
<resources>
    <color name="colorPrimary">#6200EE</color>
    <color name="colorPrimaryDark">#3700B3</color>
    <color name="colorAccent">#03DAC5</color>
    <color name="white">#FFFFFF</color>
    <color name="black">#000000</color>
</resources>
```

---

## 4. `strings.xml`

Contains all string resources used in the app, which allows for easier localization and maintenance.

### **Benefits:**
- Avoids hardcoding strings in the code
- Facilitates translation for multiple languages

### **Example:**
```xml
<resources>
    <string name="app_name">MyApp</string>
    <string name="welcome_message">Welcome to MyApp!</string>
    <string name="button_text">Click Me</string>
</resources>
```

---

## 5. `styles.xml`

This file allows you to define reusable visual properties (fonts, sizes, colors) for UI components.

### **Purpose:**
- Centralized styling for consistency
- Enables theming across widgets like buttons, text, and layouts

### **Example:**
```xml
<resources>
    <!-- Base application theme -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
    </style>

    <!-- Custom button style -->
    <style name="CustomButton">
        <item name="android:background">@color/colorAccent</item>
        <item name="android:textColor">@android:color/white</item>
        <item name="android:padding">12dp</item>
    </style>
</resources>
```

---

## 6. `themes.xml`

Defines the application-wide theme that can be applied to all activities or individually. It's more modern and modular than `styles.xml`.

### **Features:**
- Supports Material Design theming
- Defines colors, fonts, shapes, elevation, etc.

### **Example:**
```xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme -->
    <style name="Theme.MyApp" parent="Theme.MaterialComponents.DayNight.DarkActionBar">
        <!-- Primary brand color -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryVariant">@color/colorPrimaryDark</item>
        <item name="colorOnPrimary">@android:color/white</item>

        <!-- Secondary brand color -->
        <item name="colorSecondary">@color/colorAccent</item>
        <item name="colorOnSecondary">@android:color/black</item>
    </style>
</resources>
