# AirQuickUtils
AirQuickUtils provides a wide range of functions.<br/>
Text, SharedPreferences, image, network, time, location (scheduled), logs, encryption, consolidation <br/>
Various features such as SNS login (scheduled) can be used as a single library.<br/>
[![](https://jitpack.io/v/yongbeam/AirQuickUtils.svg)](https://jitpack.io/#yongbeam/AirQuickUtils)
<br/>
# Features Included
- AirLog
- AirPrefs
- AirScreen
- AirSdcard
- AirShare
- AirString
- AirSystem
- AirValidation
- AirWebView
- AirSecurity
<br/>

# Setup

### 1.Include the library as local library project.
```gradle
  allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

```gradle
  implementation 'com.github.yongbeam:AirQuickUtils:x.x.x'
```

<br/>

### 2. Add Initialization into your Application class
```java
  AirQuickUtils.init(this);
  // The log is not exposed in debug mode unless you specify. (Required)
  AirQuickUtils.setMode(BuildConfig.DEBUG);
  AirQuickUtils.setTAG("TAG NAME");
```
<br/>

# Usage
### AirPref.
##### set SharedPreferences.
```java
  AirQuickUtils.prefs.save("KEY_NAME" , "String Value");
  AirQuickUtils.prefs.save("KEY_NAME" , true);
  AirQuickUtils.prefs.save("KEY_NAME" , 10);
  AirQuickUtils.prefs.save("KEY_NAME" , 10f);
  AirQuickUtils.prefs.save("KEY_NAME" , 10L);
```
#### get SharedPreferences.
```java
  AirQuickUtils.prefs.getString("KEY_NAME" , null);
  AirQuickUtils.prefs.getBoolean("KEY_NAME" , false);
  AirQuickUtils.prefs.getInt("KEY_NAME" , 0);
  AirQuickUtils.prefs.getFloat("KEY_NAME" , 0f);
  AirQuickUtils.prefs.getLong("KEY_NAME" , 0L);
```

<br/>

### AirLog.
```java
  AirQuickUtils.log.d("LOG MESSAGE");
```

<br/>

### AirWebView.
#### 1. Add AirCommonWebViewActivity into your AndroidManifest.xml
```xml
     <!-- AirCommonWebViewActivity -->
     <activity android:name="yongbeom.utils.airquickutils.activity.AirCommonWebViewActivity"
         android:theme="@style/Theme.AppCompat" />
```

#### 2. Set AirWebViewOption
```java
    AirWebViewOption webViewOption = new AirWebViewOption();
    webViewOption.setUrl("http://www.mowa.kr");
    webViewOption.setTitle("TEST WEB VIEW");
    webViewOption.setShowActionbar(false);
    webViewOption.setShowUrl(false);
```

#### 3. call startAirCommonWebView
```java
    AirQuickUtils.webview.startAirCommonWebView(webViewOption);
```

<br/>

### AirSystem. [Class AirQuickUtils.system]
```java
  AirQuickUtils.system.getDeviceUUID();
```

<br/>

### AirScreen. [Class AirQuickUtils.screen]
```java
  AirQuickUtils.screen.getScreenDensity();
```


<br/>

### AirSdcard. [Class AirQuickUtils.sdcard]
```java
  AirQuickUtils.sdcard.createTempDir();
```



# License

    Copyright 2017 ~ 2018 LeeYongBeom

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
