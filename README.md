# Quantitizer
![Jit](https://img.shields.io/jitpack/v/github/kojofosu/Quantitizer?style=for-the-badge&color=2F9319) 

![Android Weekly](https://img.shields.io/badge/Featured%20in%20androidweekly.net%20-Issue%23479-blue?color=D35400&style=for-the-badge)
![Kotlin Weekly](https://img.shields.io/badge/Featured%20in%20kotlinweekly.net.net%20-Issue%23265-blue?color=D35400&style=for-the-badge)

:sparkles: A highly customizable quantity stepper for android projects

## Demo
<div align="left">
    <img src="https://user-images.githubusercontent.com/20203694/132069805-e0ca2c3b-e1a9-469d-87b3-26104c7b9f8b.gif" alt="demo"  width="200" height="350"/>
    <img src="https://user-images.githubusercontent.com/20203694/132068856-360e492e-95c0-4c66-be82-7895cab110c3.gif" alt="demo"  width="200" height="350"/>
    <img src="https://user-images.githubusercontent.com/20203694/132069221-0b26598e-ef8c-4516-b008-18b08b3746f5.gif" alt="demo"  width="200" height="350"/>
    <img src="https://user-images.githubusercontent.com/20203694/132069463-da915a19-007f-4c8e-a3ed-f8c6d443893e.gif" alt="demo"  width="200" height="350"/>
</div>

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

<div align="left">
<img src="https://user-images.githubusercontent.com/20203694/127779360-39fbcba6-ab72-4897-88ef-59573a005144.gif" alt="demo"  width="300" />
<img src="https://user-images.githubusercontent.com/20203694/127779355-c046c8fc-6b95-49f3-b018-5ba6ac38f568.gif" alt="demo"  width="300" />
</div>

```xml
    <com.mcdev.quantitizerlibrary.HorizontalQuantitizer
        android:id="@+id/h_q"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```

### Vertical Quantitizer

- Add `VerticalQuantitizer` in your layout xml file
<div align="left">
    <img src="https://user-images.githubusercontent.com/20203694/127779363-fc5fa535-ceeb-44a7-982b-4630073893cf.gif" alt="demo"  width="300" />
    <img src="https://user-images.githubusercontent.com/20203694/127779361-9850f052-1e06-46ba-b41d-65b96d099c33.gif" alt="demo"  width="300" />
</div>

```xml
    <com.mcdev.quantitizerlibrary.VerticalQuantitizer
        android:id="@+id/v_q"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```

### No Value Quantitizer

- Add `NoValueQuantitizer` in your layout xml file
<div align="left">
    <img src="https://user-images.githubusercontent.com/20203694/131833618-b5165019-dfff-4100-9606-8a6a9c24b167.gif" alt="demo"  width="300" />
</div>

```xml
    <com.mcdev.quantitizerlibrary.NoValueQuantitizer
        android:id="@+id/n_q"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```

#### Get quantity value
```kotlin
    var hQ: HorizontalQuantitizer = findViewById(R.id.h_q)
    var selectedValue = hQ.value    //get current value
```
#### Listener
```kotlin
        hQ.setQuantitizerListener(object: QuantitizerListener{
            override fun onIncrease() {
                Toast.makeText(this@MainActivity, "inc", Toast.LENGTH_SHORT).show()
            }

            override fun onDecrease() {
                Toast.makeText(this@MainActivity, "dec", Toast.LENGTH_SHORT).show()
            }
        })
```
### Customize Quantitizer

#### Change icons
```kotlin
    hQ.setPlusIcon(R.drawable.ic_angle_double_small_right)
    hQ.setMinusIcon(R.drawable.ic_angle_double_small_left)
```

#### Change icon backgrounds
```kotlin
    hQ.setPlusIconBackgroundColor(android.R.color.holo_red_dark)
    hQ.setMinusIconBackgroundColor(android.R.color.holo_red_dark)
```

#### Change value text and background color
```kotlin
    hQ.setValueBackgroundColor(android.R.color.holo_red_dark)
    hQ.setValueTextColor("#FFFF00")
```

#### Change icon colors
```kotlin
    hQ.setMinusIconColor("#FFFF00")
    hQ.setPlusIconColor("#FFFF00")
```


### Licensed under the [MIT License](LICENSE)

```
MIT License

Copyright (c) 2021 Kojo Fosu Bempa Edue

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
