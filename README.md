#Dev Guide Book @Adview

##Contents
[I. Register and configure SDK-KEY](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#i-register-and-configure-sdk-key)

[II.About AdViewSDK_Android-3.4.1](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#Ⅱabout-adviewsdk_android-341)

[III. Add SDK](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#iii-add-sdk)

[IV. AndroidManifest.xml text configuration](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#iv-androidmanifestxml-text-configuration)

[V. Acquire ad configurations](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#v-acquire-ad-configurations)

[VI. Create banner advertising](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#vi-create-banner-advertising)

[VII. Create interstitial advertising](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#vii-create-interstitial-advertising)

[VIII. Create opening screen ad](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#viii-create-opening-screen-ad)

[IX. Create native advertising ](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#ix-create-native-advertising)

[X. Create video advertising](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#x-create-video-advertising)

[XI. Adding Proguard-rules](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#xi-adding-proguard-rules)

[XII. Adding custom ad network](https://github.com/adview/AdViewSDK_Android-3.4.1/blob/master/README.md#xii-adding-custom-ad-network)

[XIII. Add custom ad platform](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#xii-add-custom-ad-platform)

[XIV. Contact us](https://github.com/vinith-cit/AdViewSDK_Android-3.4.1/blob/master/README.md#xiii-contact-us)



##I. Register and configure SDK-KEY
1. Visit AdView website http://www.adview.com and register Adview Account.
2. Login "My Products" page, select "Publish App”
3. Select “Android” follow the prompts to complete the relevant information About the application and you will get the sole unique SDK key
4. Click “APP management” page→Configure : enter adID in“Not set”, turn on the switch, set the capacity to 100%, click “Save”. If you need more platform please turn on the switch, click “Add ad platform” and configure those respected ids. The cumulative percentage must be 100%.you can use AdView Auction Ads. Generally recommended number of platforms is 1-3.                     
![Home page](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/I.png)

5.(Optional) if you wish to show prompt when you click on the ad - Under app management --> select "Edit" against your app, Switch on "Twice confirmation" button under "Advertising text settings".									                               
![Bidding](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/III.1.png)

![bidding-2](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/III.2.png)

**Notes:**

1. We provide you with SDK that gives you the freedom to choose your favourite advertising agency. Apart from the bidding and remnant ,other ad platforms are third- party. The App key needed should be register and apply from corresponding official website, and then configure them to the corresponding platform at Adview background.
2. If you are fresher, you don’t know much about ad platform, which ad platform to choose or which ad platform revenue is stable, we suggest you to use bidding first.
3. Bidding and remnant ads need to complement market information at background, and you will not get formal ads until pass reviewed. Before that all are test ads which do not charge.
4. Ads will be shown of only those ad platforms for which the **switch** is on against them.						
5. Only the "capacity" of those ad platforms for which the switch is on will be valid, the adplatform with higher proportion will get prior request, for all ad platforms with status as ON, the cumulative should be 100%. Other wise the your priority can't be saved.  
6. For Banner ad, full screen/interstitial , opening screen ,etc, there’s a save button at the bottom of the page. You should click the save button every time you modify a ad format, otherwise the modification is invalid .
7. **Region optimization:** 
Region optimization function means mobile phone displays the regional configured ads when it’s with in the region, while in foreign country it display foreign configured ads to meet the different demands to the maximum extent. When the region optimization function is closed, it does not distinguish between home and abroad. 


##Ⅱ.About AdViewSDK_Android-3.4.1

1. Clone or download AdViewSDK_Android-3.4.1 package to go ahead with the integration process. This package contains all files needed for smooth integration and some of the important fils include AdViewDemo,libs,umeng_res and wiyun_res.

**AdViewDemo**
This folder contains Adview demo project which includes all types of ad format (banner,interstitial,video,native,open screen) sample code with explanation.

**libs**
It contains all the .jar file SDK needed for ad platform integration. 
(Libinfo.pdf has the ad platform instructions corresponding to each jar.)

**umeng_res**
To integrate Umeng SDK, you need to put the files of umeng_res given in the AdViewSDK_Android-3.4.1 to your application resource folder, and add corresponding permissions in the Andoid manifest file.

**wiyun_res**
To integrate Wiyun SDK, you need to put the files of wiyun_res given in the AdViewSDK_Android-3.4.1 to your application resource folder, and add corresponding permissions in the Andoid manifest file.


##III. Add SDK

1. Clone or download AdViewSDK_Android-3.4.1 package here.In the AdViewSDK_Android-3.4.1 folder contains libs folder ,it contains the SDK for all ad platforms. (Libinfo.pdf has the ad platform instructions corresponding to each jar.)
2. Please copy and paste **AdViewSDK_Android.jar, android-support-v4.jar and google-play-services.jar** into your application lib folder.you'll need to integrate the Google Play Services SDK into your app.This is mandatory; without Google Play Services, the SDK cannot function.

3. In order to add new ad platforms please copy the .jar file of that particular ad platform provided by AdView to your lib folder and follow the same for all other ad platforms you would like to integrate.  

![add SDK](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/IV.png)						  
**Note :**

1. To integrate Umeng SDK, you need to put the files of umeng_res given in the AdViewSDK_Android-3.4.1 to your application resource folder, and add corresponding permissions in the Andoid manifest file.
2.To integrate Wiyun SDK, you need to put the files of wiyun_res given in the AdViewSDK_Android-3.4.1 to your application resource folder, and add corresponding permissions in the Andoid manifest file.


##IV. AndroidManifest.xml text configuration

**4.1 Add permission code**

Required permissions should be added (please refer to AndroidManifest file in the AdViewDemo project).

```
	<uses-permission android:name="android.permission.READ_PHONE_STATE" />
	<uses-permissionandroid:name="android.permission.ACCESS_COARSE_LOCATION"/>
	<uses-permissionandroid:name="android.permission.ACCESS_FINE_LOCATION" />
	<uses-permissionandroid:name="android.permission.ACCESS_WIFI_STATE" />
	<uses-permissionandroid:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
	<uses-permissionandroid:name="android.permission.READ_EXTERNAL_STORAGE"/>
```

**Note:**

-**INTERNET:** allow to visit network (required)                                                                                         
-**ACCESS_NETWORK_STATE:** allow to visit various status of mobile phone (required)                                                     
-**ACCESS_COARSE_LOCATION**: allow a procedure to visit CellID or WIFI to get the rough position.                                       
-**ACCESS_FINE_LOCATION:** allow a procedure to visit the accurate position (for example, GPS)                                           
-**ACCESS_WIFI_STATE:** allow a procedure to visit WIFI status                                                                           
-**WRITE_EXTERNAL_STORAGE:** allow a procedure to visit outside storage device and can cache ads.                                       
-**READ_EXTERNAL_STORAGE:** allow a procedure to visit outside storage device                                                           


**4.2 Add Activity declaration**

The given code should be added to in AndroidManifest file for AdView, as some platforms need to declare activity to work normal, please refer to AndroidManifest file in AdViewDemo project.  

**Configurations that adview bidding ads should add:**

```
	<service android:name="com.kyview.DownloadService" />
	<activity android:name="com.kyview.AdviewWebView" />
	<activity android:name="com.kyview.AdActivity" />
	<!-- Adiview bidding video -->
	<activity android:name="com.kuaiyou.video.vast.activity.VASTAdActivity" 
	android:hardwareAccelerated="true"
	android:screenOrientation="landscape"/>
	<activity android:name="com.kuaiyou.video.AdviewWebView"/>

```


**4.3 Appointed app channel**

Please add the below code in the AndroidMainfest file:
```
	<meta-data android:name="AdView_CHANNEL" android:value=“GFAN">
	</meta-data>
```

(You must add the above code,otherwise you application won't be able to pass the review);


##V. Acquire ad configurations

**Note:**

1. InitConfiguration serve for the overall procedure, just need to transfer once only.
2. The set methods above are optional, not required.
3. From 3.2.4 version, SDK supports setting up multiple ad slots (SDK-KEY) in one application. Take 3 ad slots of demo keyset for example, some APP would like to set different ad slots in multiple Activities, thus to statistic the user visit amount of each Activity based on the amount of ad display. If one ad slot can meet the demand of APP, then there’s no need to apply multiple ad slots.

```
	// Be sure to initialize before requesting ads, otherwise the ads cannot be used
	// set ad request configured parameter,
	//you can use default configuration : InitConfiguration. createDefault(this);
	InitConfiguration initConfig = new
	InitConfiguration.Builder(this)
	//real-time access to configuration, not required 
	.setUpdateMode(UpdateMode.EVERYTIME)
	// banner switcher can be closed
	.setBannerCloseble(BannerSwitcher.CANCLOSED)
	//interstitial switcher can be closed
	.setInstlCloseble(InstlSwitcher.CANCLOSE ) ''
	//this code is useful to get logs while testing , before uploading the application to live please delete this code .
	.setRunMode(RunMode.TEST)
	// Default situation. After setting, html5 and not-html5 ads can be received,
	while Html5Switcher.SUPPORT can only receive html5 ad .setHtml5Switcher(Html5Switcher.NONSUPPORT)
	// default situation, set interstitial to display mode, popupwindow mode can be set outside the form clickable. 	   
	setInstlDisplayMode (InstlDisplayMode. DIALOG_MODE) .build();
	// respectively request banner, interstitial, native, opening screen ad configuration, keyset can be one or more key.
	AdViewBannerManager.getInstance(this).init(initConfig,MainActivity.keySet);
	AdViewInstlManager.getInstance(this).init(initConfig,MainActivity.keySet);
	AdViewNativeManager.getInstance(this).init(initConfig,MainActivity.keySet);
	AdViewSpreadManager.getInstance(this).init(initConfig,MainActivity.keySet);
```

##VI. Create banner advertising

**6.1 Add ads through adding code**

Add a banner code to layout file,

```
	<FrameLayout
	      android:id="@+id/ad_view"
	      android:layout_width="match_parent"
	      android:layout_height="150dp"
	      android:gravity="center_horizontal" />
```

Add the following code to your activity:


```

	 //Basic Initialization
	 InitConfiguration initConfiguration = new InitConfiguration.Builder(this)
		   .setUpdateMode(InitConfiguration.UpdateMode.EVERYTIME)
		   .setBannerCloseble(InitConfiguration.BannerSwitcher.CANCLOSED)
//		   .setInstlControlMode(InitConfiguration.InstlControlMode.USERCONTROL)
//		   .setSupportHtml(InitConfiguration.Html5Switcher.SUPPORT)
		   .setRunMode(InitConfiguration.RunMode.TEST)
		   .build(); 
	
```

**Note:**

This code is useful to get logs while testing, before uploading the application to live 
please delete the this code (setRunMode(InitConfiguration.RunMode.TEST))

```	  

	 //Initialization for Banner
	 AdViewBannerManager.getInstance(this).init(initConfiguration,new String[]{SDK_KEY});      

	 // request banner ads after initialization
	 AdViewBannerManager.getInstance(this).requestAd(this,SDK_KEY, this);

	 // Gets the currently requested banner View,upload it to your own layout.
	 View view = AdViewBannerManager.getInstance(this).getAdViewLayout(this,SDK_KEY);
	 layout.addView(view);


```

**6.2 Ad Banner events handling**

To receive events from ad, **you should implement an event listener interface AdViewBannerListener**.
After you implement this listener you will get the following methods.  

```
     public interface AdViewBannerListener{

        /**
         * Use this function when the ad is clicked
         */
        public void onAdClick(String key);

        /**
         * Use this function when the ad is displayed
         */
        public void onAdDisplay(String key);

        /**
         * Use this function when the ad is closed
         */
        public void onAdClose(String key);

        /**
         * Use this function only when the ad is interrupted
         by abnormity or failure
         */
        public void onAdFailed(String key);

        /**
         * once ad is Ready while this function will triggered
         */
        public void onAdReady(String key);
    }

```

**Note:**
You can refer to the code of AdBannerActivity in AdViewDemo Project.


##VII. Create interstitial advertising

**7.1 create interstitial**

**Note:**

Since interstitial ad has a certain life cycle, Please do not wait too long after the request to call showAd method, so as to avoid invalid advertising.

Add the following code to your activity:

```
	 //Basic Initialization
	 InitConfiguration initConfiguration = new InitConfiguration.Builder(this)
			.setUpdateMode(InitConfiguration.UpdateMode.EVERYTIME)
			.setBannerCloseble(InitConfiguration.BannerSwitcher.CANCLOSED)
//			.setInstlControlMode(InitConfiguration.InstlControlMode.USERCONTROL)
//			.setSupportHtml(InitConfiguration.Html5Switcher.SUPPORT)
			.setRunMode(InitConfiguration.RunMode.TEST)
			.build(); 
```
			
**Note:**

This code is useful to get logs while testing, before uploading the application to live 
please delete the this code (setRunMode(InitConfiguration.RunMode.TEST))

```

	//Initialization for interstitual advertisement
	AdViewInstlManager.getInstance(this).init(initConfiguration,new String[]{SDK_KEY});


	// interstitial ad request after initialization, ad request and display, used alone
	AdViewInstlManager.getInstance(this).requestAd(this,SDK_KEY);

	// After ad request succeed , call the display ad
	AdViewInstlManager.getInstance(this).showAd(this,SDK_KEY);


```

**7.2 Ad Interstitial Event Handling**

To receive events from ad, **you should implement an event listener interface AdViewInstlListener**.
After you implement this listener you will get the following methods.  


```
    public interface AdViewInstlListener {
        /**
         * Use this function when the ad is clicked
         */
        public void onAdClick(String key);

        /**
         * Use this function when the ad is displayed
         */
        public void onAdDisplay(String key);

        /**
         * Use this function when the ad is disappeared
         */
        public void onAdDismiss(String key);

        /**
         * Use this function when the ad is successfully received
         */
        public void onAdReceived(String key);

        /**
         * Use this function when the ad is failed
         */
        public void onAdFailed (String key);

    }

```

**7.3 Create custom style interstitial**

You can customize the popup Intrstitial ad, please refer AdInstlActivity for the entire code 
```
	// You need to set the user-managed mode when initialization, and you must manually call the display
	//after the setting   
	InitConfiguration.setInstlControlMode(InstlControlMode.USERCONTROL);

	// request interstitial ads after initialization 
	AdViewInstlManager.getInstance(this).requestAd(this,SDK_KEY);

	// You need to call it when the ads need to be displayed, the return is not null (review)  there’s an ad to return, 
	otherwise it does not get ads.
	// The returned view can be placed in a customcontainer, such as dialog
	AdViewInstlManager.getInstance(this).getInstlView (SDK_KEY);

	// Display report method should be called when successfully display (required)
	AdViewInstlManager.getInstance(this).reportImpression(SDK_KEY);

	// When the ad is clicked, the click event handling method should be called ,otherwise there will no response(required)
	AdViewInstlManager.getInstance(this).reportClick(SDK_KEY);

```

**Note:**
You can refer to the code of AdInstlActivity in AdViewDemo Project.

##VIII. Create opening screen ad

**8.1 Create opening screen ad**

Add the following code to your activity:

```
	//Basic Initialization
	InitConfiguration initConfiguration = new InitConfiguration.Builder(this)                
			.setUpdateMode( InitConfiguration.UpdateMode.EVERYTIME)
			.setBannerCloseble(InitConfiguration.BannerSwitcher.CANCLOSED)
//			.setInstlControlMode(InitConfiguration.InstlControlMode.USERCONTROL)
//			.setSupportHtml(InitConfiguration.Html5Switcher.SUPPORT)
			.setRunMode(InitConfiguration.RunMode.TEST)
			.build();
```		
**Note:**
This code is useful to get logs while testing, before uploading the application to live 
please delete the this code (setRunMode(InitConfiguration.RunMode.TEST))

```
	//Intialization for Open Screen ad
	AdViewSpreadManager.getInstance(this).init(initConfiguration, new String[]{SDK_KEY});


	// Set the logo at the bottom of opening screen (not required), you can also upload local images or images link.
	AdViewSpreadManager.getInstance(this).setSpreadLogo(R.drawable.spread_logo);

	// Set background color of opening screen( not required)
	AdViewSpreadManager.getInstance(this).setSpreadBackgroudColor( Color.WHITE);

	// Request opening screen ads
	AdViewSpreadManager.getInstance(this).request(this,SDK_KEY,(RelativeLayout) findViewById(R.id.spreadlayout), this);

```

**8.2 Ad Opening screen Event Handling**

To receive events from ad, **you should implement an event listener interface AdViewSpreadListener**.
After you implement this listener you will get the following methods.  


```
    public interface AdViewSpreadListener {
        /**
         * This function is called when the ad is displayed.
         */
        public void onAdDisplay(String key);

        /**
         * This function is called when the ad requestsucceeds.
         */
        public void onAdReceived(String key);

        /**
         * Click to callback .
         */
        public void onAdClick(String key);

        /**
         * This function is called when the ad request failed.
         */
        public void onAdFailed(String key);

        /**
         *This function is called when the ad is closed.
         */
        public void onAdClose(String key);

        /**
         * Custom callback
         */
        public void onAdNotifyCustomCallback(String key,ViewGroup view,int ruleTime,int delayTime);

    }


```

**8.3 Custom countdown notification style on the top of opening screen**
#Action needed 

```
	// Skip button will appears on the top after settings
	AdViewSpreadManager.getInstance(this).setSpreadNotifyType(this, AdSpreadManager.NOTIFY_COUNTER_NUM);

	// Defaults, none notification will be displayed
	public final static int NOTIFY_COUNTER_NULL = 0;

	// Countdown will be shown after settings
	public final static int NOTIFY_COUNTER_NUM = 1;

	// Skip button will be shown on the top after settings,but it will appear only after specified times.
	public final static int NOTIFY_COUNTER_TEXT = 2;

	// Will call this after settings:onAdNotifyCustomCallback(String key,ViewGroup view,intruleTime,int delayTime) interface, you 
	//can custom notification styles
	public final static int NOTIFY_COUNTER_CUSTOM = 3;

```

**Note:**

For opening advertising please make sure the exposure time is sufficient, otherwise it will affect the ad revenue. You can refer to the code of SpreadScreenActivity in AdViewDemo Project.

##IX. Create native advertising 

**9.1 create native advertising**

Add a listview to layout file, e.g :

```
	<ListView
	   android:id="@+id/list"
	   android:layout_width="match_parent"
	   android:layout_height="match_parent" />

```

Add the following code to your activity:

```
	//Basic Initialization
	InitConfiguration initConfiguration = new InitConfiguration.Builder(this)                
			.setUpdateMode( InitConfiguration.UpdateMode.EVERYTIME)
			.setBannerCloseble(InitConfiguration.BannerSwitcher.CANCLOSED)
//			.setInstlControlMode(InitConfiguration.InstlControlMode.USERCONTROL)
//			.setSupportHtml(InitConfiguration.Html5Switcher.SUPPORT)
			.setRunMode(InitConfiguration.RunMode.TEST)
			.build();
```			
**Note:**

This code is useful to get logs while testing, before uploading the application to live 
please delete the this code (setRunMode(InitConfiguration.RunMode.TEST))

```
	//Intialization for Native advertisement
	AdViewNativeManager.getInstance(this).init(initConfiguration,new String[]{SDK_KEY});


	//Initialized native ads should custom ad layout in advance, and apply native ad ID at app background
	AdViewNativeManager.getInstance(this).requestAd(this,SDK_KEY, 2,this); 

	//set native callback interface
	@Override
	public void onReceivedAd(String key,List arg0) {
	for (int i = 0; i < arg0.size(); i++) { 
		Data data = newData();
		NativeAdInfo nativeAdInfo = (NativeAdInfo) arg0.get(i);
		data.descript = nativeAdInfo.getDescription(); 
		data.icon = nativeAdInfo.getIconUrl();
		data.title = ((NativeAdInfo) arg0.get(i)).getTitle();
		data.adInfo = (NativeAdInfo) arg0.get(i);
		((NativeAdInfo) arg0.get(i)).getIconHeight();
		data.isAd = true;
		Log.i("native information ", "data.descript: " + data.descript + "\ndata.icon: " + data.icon + "\ndata.title:" + 
		data.title); 
		list.add(3, data);
		((NativeAdInfo) arg0.get(i)).onDisplay(newView( AdNativeActivity.this));
		} 
	}

	/**
	 * This function is called when the ad requests failed.
	 */
	@Override
	public void onFailedReceivedAd(String arg0) {
	}
	/**
	 * This function is called when download ads, to back to
	   the status of current downloading contents.
	 */
	@Override
	public void onAdStatusChanged (int arg0) {
	}
	});

```

**9.2 Ad Native Event Handling**
To receive events from ad, **you should implement an event listener interface AdViewNativeListener**.
After you implement this listener you will get the following methods.  


```
    public interface AdViewNativeListener {

        /**
         * This function is called when the ad request succeed.
         */
        public void onAdReceived(String key, List<NativeAdInfo> adMaps);

        /**
         * This function is called when ad request failed.
         */
        public void onAdReceived(String key);

        /**
         * When the ad status changed.
         */
        public void onAdStatusChanged(String key, int status);

    }

```

##X. Create video advertising
**10.1 create video advertising**

Add the following code in activity,

```
	//Basic Initialization
	InitConfiguration initConfiguration = new InitConfiguration.Builder(this)                
			.setUpdateMode( InitConfiguration.UpdateMode.EVERYTIME)
			.setBannerCloseble(InitConfiguration.BannerSwitcher.CANCLOSED)
//			.setInstlControlMode(InitConfiguration.InstlControlMode.USERCONTROL)
//			.setSupportHtml(InitConfiguration.Html5Switcher.SUPPORT)
			.setRunMode(InitConfiguration.RunMode.TEST)
			.build();

```
**Note:**

This code is useful to get logs while testing, before uploading the application to live 
please delete the this code (setRunMode(InitConfiguration.RunMode.TEST))

```
	//Initialization For Video ads
	AdViewVideoManager.getInstance(this).init(initConfiguration,new String[]{SDK_KEY});

	//Request video ads after initialization. Request and display ads should be used separately.
	AdViewVideoManager.getInstance(this).requestAd(this,SDK_KEY,this);

	//set video callback interface
	// Call display ad after ad request succeed.
	AdViewVideoManager.getInstance(this).playVideo(this,SDK_KEY);

```

**10.2 Ad Video Event Handling**

To receive events from ad, **you should implement an event listener interface AdViewVideoListener**.
After you implement this listener you will get the following methods.  


```
    public interface AdViewVideoListener{
        
        /**
         * Play start event notification
         */
        public void onAdPlayStart(String key);

        /**
         * Play end event notification
         */
        public void onAdPlayEnd(String key, Boolean isEnd);

        /**
         * Close event notification
         */
        public void onAdClose(String key);

        /**
         * Request succeed notification
         */
        public void onAdReceived(String key);

        /**
         * Request failed notification
         */
        public void onAdFailed (String key);
        
    }


```

**Note:**

You can refer to the code of AdVideoActivity in AdView Demo Project.

##XII. Adding custom ad network
![Inmobi 1](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/inmobi%201.png)
![Inmobi 2](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/inmobi2.jpg)
![Inmobi 3](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/inmobi3.jpg)
![Inmobi 4](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/inmobi4.jpg)
![Inmobi 5](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/inmobi5.jpg)





##XI. Adding Proguard-rules 

If you have a ProGuard configuration file please add the below lines of code in proguard-rules.pro file

```
	-keep public class com.kyview.** {*;} 
	-keep public class com.kuaiyou.** {*;} 

```
In case you add other adnetworks ( like InMobi, AdMob etc..,) add their proguard rules to proguard-rules.pro file.

For example In case of InMobi add the below lines of code to the proguard-rules.pro.
```
	-keep class com.google.android.gms.ads.identifier.AdvertisingIdClient{
	    public *;
	}

	-keep class com.google.android.gms.ads.identifier.AdvertisingIdClient$Info{
	    public *;
	}

	-keep class com.inmobi.**
	{ *; }

	-dontwarn com.inmobi.**

```

##XII. Add custom ad platform

Sometimes developers would like to add a platform which is not aggregated, Adview provide ways to meet this demand.

There’s a “Custom ad platform” in add ad platform . Developer needs to fill in app ID1, this is the name of a function which needs client side to complete. The function of this function is to call the ad platform interface . As for App ID2, just fill in something, otherwise you cannot save it.
 
 
![custom ad platform](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/custom%20platform1.png)

![custom add platform2](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/custom%20platform%202.png)
 

 **11.1 For Custom platform (Amazon) function implementation**    
 

```
	// you can visit https://developer.amazon.com/sdk/mobileads.html
	// Must with: final AdViewAdapter adapter, final String key these two parameter
	// Otherwise will result in the failure in custom ad

	public void amazon_proc(final AdViewAdapter adapter,final String key){

	// TODO Auto-generated method stub
	AdRegistration.enableLogging(this, true);
	AdRegistration.enableTesting(this, true);
	AdRegistration.setAppKey(this, "sample-app- v1_pub-2");

	// Create an example of amazon in adview
	adView = new AdLayout(this, AdSize.AD_SIZE_320x50);

	//appointed listen interface
	adView.setListener(new AdListener() {
	@Override
	Log.d("AdViewSample", arg1.getAdType().toString()+ " Ad loaded successfully.");

	// after the ad request succeed, start the timer and request another ad when time’s up.
	adapter.reportImpression(key);
	adapter.rotateDelayedAd(key);
	}
	@Override
	public void onAdExpanded(AdLayout arg0) {
	// TODO Auto-generated method stub
	}
	@Override
	public void onAdCollapsed(AdLayout arg0) {
	// TODO Auto-generated method stub
	}
	@Override
	public void onAdFailedToLoad(AdLayout arg0, AdError arg1) {
	// TODO Auto-generated method stub
	Log.w("AdViewSample","Ad failed to load. Code: "+ arg1.getResponseCode() +", Message: "+arg1.getResponseMessage());

	// start to request another ad when failed.
	adapter.rotatePriAd(key);
	}
	});
	AdViewBannerManager.getInstance(AdBannerActivity.this).addSubView(AdViewBannerManager.getInstance(AdBannerActivity.this) .
	getAdViewLayout(AdBannerActivity.this,key), adView, key); 
	AdTargetingOptions adOptions = new AdTargetingOptions(); 
	adView.loadAd(adOptions);

	}

```
**You can refer the code in AdViewDemo project --> BannerActivity for implementation of Amazon ad; ** 

##XIII. Contact us 

Users can login Adview, there are service E-mail, service contact number and enterprise QQ customer service at the bottom of the homepage 

![custom ad platform](https://raw.githubusercontent.com/vinith-cit/Images-for-github/master/VII.png)


