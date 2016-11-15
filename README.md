# Facebook Live Video Polling
Useful features:
* Automatically update reaction count from Facebook Graph API
* Basic CSS Animations
* Responsive - resizes to any browser size perfectly

... and *more*! :+1:

![FBLivePoll Demo](http://i.imgur.com/Vy5Kepg.png)
> Basic demo of FBLivePoll

## Getting Started
#### Step 1. Facebook Graph Access Token
You'll need to set up a new App in Facebook (see the guide [here](https://developers.facebook.com/docs/marketing-api/authentication), see the section labeled 'Obtain Permanent Page Access Token'). Choose "Website" as the Application type. Copy your Access Token for your app and insert it at the top of the 'reactions.php' file. This is also where you'll put the ID of your Live Video in Step 3.

```php
$videoid="VIDEO_ID_HERE"; 
// The ID of the Live Video
$access_token="ACCESS_TOKEN_HERE"; 
// Your Facebook app's access token in the format 1111111111111111|X1xX11xX_XXXxXxXXX1xXXx1XXX
```

#### Step 2. Customise the appearance of the 'reactions.html' file
- The background image and appearance can be customised in 'style.css'
- The options and symbols can be customised in 'reactions.html'. Reaction icons are included
- The 'reactions.html' file is based on Bootstrap. For more information on the Bootstrap grid system, [read the Bootstrap docs](http://getbootstrap.com/css/#grid)

#### Step 3. Add 'reactions.html' as source in OBS
Upload the files to a web server and point OBS (or the broadcast software of your choice) to the URL of your 'reactions.html' file, using it as a source. You may use the BrowserSource plugin for OBS, or open the page in a new browser window and use a Window based source.

Still need to choose a software package to go Live with? [Facebook]((https://www.facebook.com/facebookmedia/get-started/live)) has a list of compatible software.

#### Step 4. Go Live!
Don't forget to add your Video ID to the top of the 'reactions.php' file! As soon as it's added, the 'reactions.html' file should reflect the reaction count, without having to refresh the browser.

Going live isn't in the scope of this readme - more information on how to go live using a software package of your choice is [available from Facebook](https://www.facebook.com/facebookmedia/get-started/live)


##### Feel like a tinker?

FBLivePoll is based on [Bootstrap](http://getbootstrap.com) and uses the Facebook [Graph API](https://developers.facebook.com/docs/graph-api) to fetch reactions. Build on it, make something amazing! [Let me know](mailto:hayden@gennext.net.au) what you make, I'd love to see!


##### Troubleshooting

If no values are displayed, ensure the Facebook Access Token entered is correct (it should be in the format 1111111111111111|X1xX11xX_XXXxXxXXX1xXXx1XXX, where 1 is a number and x is a letter.)

If you're still having problems, ensure CURL is correctly configured in your environment and that all file permissions are correct.

[Email Me](mailto:hayden@gennext.net.au) if you have any issues - otherwise, let me know what you've made - I'd love to see it in action!
