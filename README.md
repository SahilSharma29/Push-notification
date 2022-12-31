# Push-notification

In app.js file 
  useEffect(() => {
    requestUserPermission();
    notificationListener();
  }, []);
  
  // call Foregroundhandler component like this
  
  <Provider store={store}>
      <NavigationContainer ref={navigationRef}>
        <SafeAreaProvider>
          <PersistGate persistor={persistor}>
            <ForegroundHandler /> --------> like this
            <AppView />
          </PersistGate>
        </SafeAreaProvider>
      </NavigationContainer>
    </Provider>
    
     
    use library for foreground
    @react-native-community/push-notification-ios
    react-native-push-notification
    
    after installing follow doc for android and ios 
    but in android mainfest.xml after follow doc
    if you get error on build then change this code (android:exported="false") in last reciever
    
     <receiver android:exported="false" android:name="com.dieam.reactnativepushnotification.modules.RNPushNotificationBootEventReceiver">
            <intent-filter>
                <action android:name="android.intent.action.BOOT_COMPLETED" />
                <action android:name="android.intent.action.QUICKBOOT_POWERON" />
                <action android:name="com.htc.intent.action.QUICKBOOT_POWERON"/>
            </intent-filter>
        </receiver>
        
        
      I assume that you already setup firebase if not then follow doc orr some video .
