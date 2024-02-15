# Android Build

The keystore file plays a crucial role in ensuring the secure and unique signing of your application binary. This prevents other apps pretending to be updates for your app. When you submit an update to Google Play, the new version binary must be signed with the same keystore file used in the original build.

Documentation: https://docs.appgyver.com/docs/android-builds

---------------------------------------------------------------

## Step-by-step:

1) Install [Java](https://www.oracle.com/java/technologies/javase/jdk15-archive-downloads.html) if you don't already has it installed;
2) Open your Terminal/Command Line Prompt;
3) Navigate to the folder which you want to create the .keystroke file within:
     ```shell
   cd path/to/directory
     ```
5) Run the following command:
   ```shell
   keytool -genkey -v -keystore my-app-name.keystore -alias my-app-name -keyalg RSA -keysize 2048 -validity 10000
   ```
    Don't forget to change the `my-app-name` for your actual app name.
7) You will be prompted to enter a password;
8) It will ask you for further optional information;
9) When finished, you will have the following information to enter to AppGyver:
   - **Keystore File** - It's your `my-app-name.keyword`. It will be located in the folder where you ran the `keytool` command;
   - **Keystore Password** - It's the password you entered;
   - **Keystore Alias** - This is the `my-app-name`.
