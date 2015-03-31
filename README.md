## To install:

```
cordova plugin add org.ogury.cordova.plugin --variable API_KEY=your_api_key
```

## To use:

```
var app = {
  onDeviceReady: function() {
    CPresage.adToServe(app.onAdEvent, app.onAdNotFound);
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

## To use with phonegap build:

```
  <gap:plugin name="org.ogury.cordova.plugin" source="plugins.cordova.io">
    <param name="API_KEY" value="your_api_key" />
  </gap:plugin>
```  

See Ogury admin panel for more details

## Licence

The MIT License (MIT)

Copyright (c) 2015 Fergal Condron

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
