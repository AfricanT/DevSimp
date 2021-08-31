
# DevOps Project Android CI CD Deploy build to App Center

##### Below are the Steps for creating this project .

##### Installation of Android SDK on Ubuntu 18.04 and setup the configration 

```sh

sudo apt-get update

sudo apt install openjdk-8-jdk -y

sudo apt install android-sdk

sudo mkdir /usr/lib/android-sdk/cmdline-tools

cd /usr/lib/android-sdk/cmdline-tools

sudo  wget https://dl.google.com/android/repository/commandlinetools-linux-6609375_latest.zip

sudo unzip commandlinetools-linux-6609375_latest.zip 

sudo rm commandlinetools-linux-6609375_latest.zip  

rm commandlinetools-linux-6609375_latest.zip 

export ANDROID_HOME=/usr/lib/android-sdk/

export PATH=$PATH:$ANDROID_HOME/cmdline-tools/tools/bin

export PATH=$PATH:$ANDROID_HOME/platform-tools

sdkmanager --version

sdkmanager --list

sudo chmod 777 $ANDROID_HOME -R

yes | sdkmanager --licenses

yes | sdkmanager "platform-tools" "platforms;android-29"

```


##### SetUp Java and Android Path 

```sh

Goto Manage Jenkins ->  Global Tool Configration 

Setup Java Path in Env, 

JAVA Default Location = /usr/lib/jvm/java-8-openjdk-amd64/

Click Save and Apply and Back button 

Click on Configration - in Env. Set the Android_SDK path  

ANDROID_HOME = /usr/lib/android-sdk/


```


##### Setup Path in Jenkins


```sh


JAVA Default Location = /usr/lib/jvm/java-8-openjdk-amd64/

Click Save and Apply and Back button 

Click on Configration - in Env. Set the Android_SDK path  

ANDROID_HOME = /usr/lib/android-sdk/


```

##### SetUp AppCenter Account 

```sh

Create the account in AppCenter 

Copy the API Key from -> Account Setting  -> User API token -> Click on New API -> Provide the name and Allow all the access and copy the token

Goto Dashboard -> Click on Add New - >

                    1. Click on Add New App
                    2. Provide the App Name.
                    3. Release Type 
                    5. OS type 
                    6. Platform 
After Creating App 
          1. Click on Distribution 
          2. Click on Group 
          3. Create the New Group

Copy the User name from ->  Account Setting 

```

##### Post Build setting to App Center 

```sh

1. Provide the API token 
2. Provide the App Name 
3. Provide the APK path 
4. Provide the Group Name 
```
