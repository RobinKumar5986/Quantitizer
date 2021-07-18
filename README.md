# Quantitizer
![Jit](https://img.shields.io/jitpack/v/github/kojofosu/Quantitizer?style=for-the-badge) 

:sparkles: A quantity stepper for android projects

## Setup

Add it in your root `build.gradle` at the end of repositories:

```groovy
allprojects {
    repositories {
        //...omitted for brevity
        maven { url 'https://jitpack.io' }
    }
}
```



Add the dependency

```groovy
dependencies {
   implementation "com.github.kojofosu:Quantitizer:$latest_release"
}
```

## Usage
Sample implementation [here](app/)

### Horizontal Quantitizer

- Add `HorizontalQuantitizer` in your layout xml file

<img src="https://user-images.githubusercontent.com/20203694/126061466-a4a98491-c0ad-4af9-bfde-f4ee486531ff.gif" alt="demo"  width="400" />

```xml
    <com.mcdev.quantitizerlibrary.HorizontalQuantitizer
        android:id="@+id/h_q"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```

