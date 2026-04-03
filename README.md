Samsung Health Stack – ResearchStack App 
Overview 
This project demonstrates integration with Samsung Health Sensor SDK to collect health 
data from Samsung Galaxy Watch and sync it with an Android mobile application. 
The app connects to a Samsung wearable device, retrieves sensor data such as heart rate 
and activity metrics, and displays it inside the Android application. The system uses 
Samsung’s privileged health tracking APIs for real-time communication between watch and 
phone. 
Features 
• Connect Samsung Galaxy Watch to Android phone 
• Retrieve real-time sensor data 
• Sync health metrics from watch to mobile app 
• Display live health tracking values 
• Wireless debugging support 
• Background data sync 
• Wearable + Mobile integration 
Project Structure 
app-sdk/ 
├ auth 
├ backend-integration 
├ libs/privsdk 
├ samples 
├ privsdkwrapper 
└ common 
The libs/privsdk folder contains required Samsung Health SDK .aar files. 
Requirements 
Hardware Requirements 
• Samsung Galaxy Phone (One UI supported) 
• Samsung Galaxy Watch (Wear OS) 
• Same WiFi network (Phone + Laptop) 
• Bluetooth enabled 
Recommended devices: 
• Galaxy Watch 4 / 5 / 6 
• Samsung Galaxy S series / A series 
Software Requirements 
• Android Studio (latest) 
• Java 17 / Kotlin support 
• Android SDK 33+ 
• ADB installed 
• Samsung Health Sensor SDK (.aar files) 
• Wireless Debugging enabled 
Required Samsung SDK Files 
Place the following file in: 
app-sdk/libs/privsdk/ 
Required file: 
samsung-health-sensor-api-v1.3.0.aar 
Then sync Gradle. 
How the App Works 
1. App starts on Android phone 
2. App connects to Samsung Watch 
3. Watch sensors start collecting data 
4. Data sent using Samsung Health SDK 
5. Mobile app receives sensor stream 
6. Data displayed in UI 
7. Data stored locally / processed 
Setup Instructions 
Step 1 — Clone Repository 
git clone <your-repo-url> 
cd app-sdk 
Step 2 — Open in Android Studio 
Open project: 
File → Open → app-sdk 
Wait for Gradle sync. 
Step 3 — Add Missing Samsung SDK 
Copy .aar file into: 
app-sdk/libs/privsdk/ 
Then click: 
Sync Project with Gradle Files 
Connecting Samsung Phone 
Enable developer options: 
Settings → About phone → Tap Build Number 7 times 
Then enable: 
Developer Options → Wireless Debugging 
Pair device: 
adb pair IP:PORT 
adb connect IP:PORT 
Verify: 
adb devices 
Connecting Samsung Watch 
Step 1 
Pair watch with phone using Galaxy Wearable app 
Step 2 
Enable developer mode on watch: 
Settings → About Watch → Software → Tap version 7 times 
Step 3 
Enable: 
Developer Options → ADB debugging 
Wireless debugging 
Step 4 
Connect watch using ADB 
adb connect WATCH_IP:PORT 
Running the App 
1. Connect phone using ADB 
2. Connect watch using ADB 
3. Run Android app 
Android Studio: 
Run ▶ 
Select device: 
Samsung phone 
App will install. 
Data Sync Flow 
Samsung Watch 
↓ 
Sensor API 
↓ 
Samsung Health SDK 
↓ 
Phone App 
↓ 
UI Display 
↓ 
Local Storage 
Syncing Health Data 
The app syncs: 
• Heart rate 
• Steps 
• Activity 
• Motion sensors 
• Health metrics 
Sync happens: 
• Real-time streaming 
• Background service 
• Manual refresh 
Troubleshooting 
Device not showing 
Run: 
adb devices 
Reconnect. 
Missing AAR file 
Add: 
samsung-health-sensor-api-v1.3.0.aar 
Watch not connecting 
Ensure: 
• Same WiFi 
• Debugging enabled 
• Bluetooth ON 
Build 
Debug build: 
Build → Build APK 
APK location: 
app/build/outputs/apk/debug/ 
Tech Stack 
• Android (Kotlin) 
• Samsung Health Sensor SDK 
• Wear OS 
• ADB Wireless Debugging 
• Gradle Kotlin DSL 
Author 
Nikhil Bhosale 
Samsung Health Stack Research Project 
License 
Samsung Privileged SDK required 
For research and development use only 
