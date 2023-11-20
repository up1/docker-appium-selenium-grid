## Working with Docker compose
* Selenium Hub
* Appium android node
  * Start android emulator
 



### 0. Check android devices
```
$adb devices
```

### 1. Start Selenium Hub
```
$docker compose up -d selenium_hub
```

Go to Selenoum Hub
* http://localhost:4444

### 2. Start Appium server with Android device
```
$docker compose up -d appium_android_device
```

### 3. Start Selenium Node and register to Selenium Hub
```
$docker compose up -d selenium_node
```

```
$docker compose ps                 
NAME                                  IMAGE                  COMMAND                  SERVICE                 CREATED          STATUS          PORTS
appium-grid-appium_android_device-1   appium/appium          "appium --config /ho…"   appium_android_device   2 minutes ago    Up 2 minutes    0.0.0.0:4723->4723/tcp
appium-grid-selenium_hub-1            selenium/hub           "/opt/bin/entry_poin…"   selenium_hub            11 minutes ago   Up 10 minutes   4442-4443/tcp, 0.0.0.0:4444->4444/tcp
appium-grid-selenium_node-1           selenium/node-docker   "/opt/bin/entry_poin…"   selenium_node           7 minutes ago    Up 4 seconds    4444/tcp
```

### Reference Websites
* https://github.com/appium/appium-docker-android
* https://www.somkiat.cc/selinium-grid-4-and-appium/
* https://gist.github.com/up1/834448e8d6560f5b69a0ed26ed51d48a


