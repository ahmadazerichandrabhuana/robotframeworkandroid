# Test Automation for Android Apps using Robot Framework

This is a sample Test Automation for Android Apps using Robot Framework with Appium Library inside it.

## Requirements

1. Install [Python 3](https://www.python.org/).
2. Make sure 'pip' also installed together with Python 3. If it is not automatically installed, refer to [Python Crash Course](https://ehmatthes.github.io/pcc/chapter_12/installing_pip.html).
3. Update Python to your PATH file. Refer [here](https://realpython.com/add-python-to-path/), this website covered configuration for Windows, Linux, and MacOS.
4. Install [RobotFramework](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#installing-using-pip), or simply run below command :
   ```
    pip install -r requirements.txt
   ```
5. Install [JDK](https://www.oracle.com/id/java/technologies/downloads/).
6. Install [Android Studio](https://developer.android.com/studio/install).
7. Update JAVA_HOME and ANDROID_SDK_ROOT to yout PATH file. There is no easy way to explain this. You can refer [here](https://medium.com/@omurdenden/set-java-home-and-bin-directory-for-appium-testing-in-macos-f8cee3fe56b4) or Google it.
8. Install [Node](https://nodejs.org/en/download/package-manager).
9. Install [Appium](https://appium.io/docs/en/2.2/quickstart/install/).
10. Install and run [appium-doctor](https://www.npmjs.com/package/appium-doctor) to make sure all your appium's dependecies are OK.
11. Download and install [Demo Apps](https://github.com/saucelabs/my-demo-app-rn/releases).
12. Install [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/).
13. Recommended Code Editor : [VS Code](https://code.visualstudio.com/), but you're welcome to use any Code Editor you're comfort with.

## Device Connection

Connect your device to your computer, check it's udid : 
```
adb devices
```
Put it on file 'env.yaml' line 7 : 
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
   robot tests/{test file name using extention ".robot"}
   sample :
   robot tests/001.robot
   ```

## Open Test Report

    open report.html

## Open Test Log

    open log.html

## Repository Explanation

This sample Test Automation consists of 3 main folders : 

* config
   ```
   Contains very basic config of Variables, Settings, and Keyword wich will be used globally on other files
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

Apart from these 3 folders, this sample also using 'env.yaml' file to store configuration-specific data.
