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

### Vertical Quantitizer

- Add `VerticalQuantitizer` in your layout xml file

<img src="https://user-images.githubusercontent.com/20203694/126719791-44a7393d-738f-4c66-94a5-30df087705b5.gif" alt="demo"  width="400" />

```xml
    <com.mcdev.quantitizerlibrary.VerticalQuantitizer
        android:id="@+id/v_q"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
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
