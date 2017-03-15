# GmailAuthApiTest
The app demonstrates the use of the gmailauth library included in the repository.

## Add a Library

Requirements device with Android API > 16 and a updated browser that supports Chrome Custom Tabs on Android e.g. Chrome.

The library is tested on Android SDK 23+ 

Thus            
            
             previous: minSdkVersion 23

Updated: Tested on Moto G Android SDK 22
            
            minSDKVersion 16.
            
Change the values in your app/build.gradle and gmailauth/build.gradle.

Clone the Repository

Copy or Add the gmailauth folder to your app in Android Studio.

Right Click on your app module and click Open Module Settings.

Select the module in the left pane and open Dependencies. Click '+' at the bottom left and select
add Module Depency and select the gmailauth module.

##Future
Library will be published to jcenter() and instructions for adding using gradle will be added.

## Library Features.
It is a ready to use UI and logic for add Gmail Authentication to your app.

It uses data binding library.

###############################################################################
 Include the following in the build.gradle in your app module
                      
            android {
               ...
                dataBinding {
                    enabled = true
                }
              }
The UI can be customised by changing the values

################################################################################
        colors.xml
        
        <?xml version="1.0" encoding="utf-8"?>
        <resources>
            <color name="colorPrimary">#2196F3</color>
            <color name="colorPrimaryDark">#303F9F</color>
            <color name="colorAccent">#E040FB</color>
            <color name="colorTitleTextPrimary">@android:color/white</color>
            <color name="colorTextPrimary">@android:color/black</color>
            <color name="colorButtonTextPrimary">@android:color/white</color>
            <color name="colorTextSecondaryPrimary">@android:color/black</color>
        </resources>
##################################################################################
        styles.xml
        
        <resources>
          <!-- Base application theme. -->
          <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
              <!-- Customize your theme here. -->
              <item name="colorPrimary">@color/colorPrimary</item>
              <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
              <item name="colorAccent">@color/colorAccent</item>
              <item name="titleTextColor">@color/colorTitleTextPrimary</item>
              <item name="android:typeface">sans</item>
          </style>

      </resources>
 
 The UI provides custom layout for portrait and landscape view(Suitable for phones currently)
 
 You can invole the library from your app in the following way
  
            Intent intent = new Intent(this,GmailAuthActivity.class);
            intent.setFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
            startActivity(intent);
  
  The token response after login can be sent to Servers for further Use. The class SendTokenTask, uses Https to send data to servers. Currently it points to a Dummy URL.(MalformedUrlException is caught, so the app does not crash).
  
  ![Alt text](http://i.imgur.com/qaJ0wup.png "Login Screen") ![Alt text](http://i.imgur.com/M721HkK.png "Account Chooser") ![Alt text](http://i.imgur.com/yYfM9b7.png "Logged In")
  
