# Test Automation for Android Apps using Robot Framework

This is a sample Test Automation for Android Apps using [Robot Framework](https://robotframework.org/) with Appium Library inside it.

## Requirements

1. Install [VS Code](https://code.visualstudio.com/) or any Code Editor you're comfort with.
2. Install [python](https://www.python.org/), preferably version **3.9.10** (that's the one I used and having no issue).
3. Make sure `pip` also installed together with python. If it is not automatically installed, refer to [Python Crash Course](https://ehmatthes.github.io/pcc/chapter_12/installing_pip.html).
4. Update python to your PATH file. Refer [here](https://realpython.com/add-python-to-path/), this website covered configuration for Windows, Linux, and MacOS. Or, if you prefer using python version management tools, refer to [this article](https://medium.com/@zorozeri/how-to-install-pyenv-and-manage-pythonversion-on-your-local-machine-241b119b7ae9) for using [pyenv](https://github.com/pyenv/pyenv).
5. Download and open this code repository on your local Code Editor and run this commands :
   ```
   pip install -r requirements.txt
   ```
6. Install [JDK](https://www.oracle.com/id/java/technologies/downloads/).
7. Install [Android Studio](https://developer.android.com/studio/install), and install Android SDK using Android Studio.
8. Update JAVA_HOME and ANDROID_HOME to yout PATH file. There is no easy way to explain this. You can refer [here](https://medium.com/@omurdenden/set-java-home-and-bin-directory-for-appium-testing-in-macos-f8cee3fe56b4) or Google it.
9. Install [Node](https://nodejs.org/en/download/package-manager).
10. Install [Appium](https://appium.io/docs/en/2.2/quickstart/install/) and install appium driver `uiautomator2`.
11. Install and run [appium-doctor](https://www.npmjs.com/package/appium-doctor) to make sure all your appium's dependencies are OK, trouble shoot if any red "x" appears (you need to google it yourself).
12. Install [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/), or add ADB installed from Android Studio into your PATH file.
13. Download and install this [Demo Apps](https://github.com/saucelabs/my-demo-app-rn/releases)(`.apk` file) into your Android Device (credit to [Wim Selles](https://github.com/wswebcreation)).

## Device Connection

Connect your device to your computer, check it's udid : 
```
adb devices
```
Put it on file `env.yaml` line 7 : 
```
udid: {your device udid}
sample : 
udid: emulator-5554
```

## Run Tests
* Run all tests : 
   ```
   robot tests
   ```

* Run specific test : 
   ```
   robot tests/{test file name using extension ".robot"}
   sample :
   robot tests/001.robot
   ```

## Open Test Report
   MacOs : 

    open report.html
   Windows : 

    start report.html
   Or just drag and drop file `report.html` into your Browser.

## Open Test Log
   MacOs : 

    open log.html
   Windows : 

    start log.html
   Or just drag and drop file `log.html` into your Browser.

## Short Repository Explanation

This sample Test Automation consists of 3 main folders : 

* config
   ```
   Contains basic configuration of Variables, Settings, and Keyword wich will be used globally on this whole project
   ```
* resources
   ```
   Consists of 3 more folders :
   > helpers  : contains any action which might be used globally on any pages
   > locators : contains web element for each specific web pages
   > pages    : contains actions which will be performed on each specific web pages
   ```
* tests
   ```
   Contains test cases
   ```

Apart from these 3 folders, this sample also using `env.yaml` file to store configuration-specific data.

## Appium Library Keywords Documentation

https://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html
