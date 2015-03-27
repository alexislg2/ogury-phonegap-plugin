To install:

```
cordova plugin add org.ogury.cordova.plugin --variable API_KEY=your_api_key
```

To use:

```
var app = {
  onDeviceReady: function() {
    Ogury.adToServe(app.onAdEvent, app.onAdNotFound);
  },
  onAdEvent: function(event) {
    console.log('onAdEvent called here');
    if(event == 'AdFound') {
      console.log('AD FOUND');
      // If you want to do specific stuff when an ad is about to be displayed, even just a log
    } else if (event == 'AdClosed') {
      console.log('AD CLOSED');
      // If you want to do specific stuff when an ad is clicked or dismissed, even just a log
    }
  },
  onAdNotFound: function(error) {
    console.log('AD NOT FOUND');
    // If you want to do specific stuff when no ad to display, even just a log
  }

}
```

To use with phonegap build:

```
  <gap:plugin name="org.ogury.cordova.plugin" source="plugins.cordova.io">
    <param name="API_KEY" value="your_api_key" />
  </gap:plugin>
```  

See Ogury admin panel for more details
