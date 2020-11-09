This package fetches a Instagram users media using the Instagram Basic Display API.

The package handles Instagram Authentication then returns the users media including the captions, ids, media urls, timestamps, and media types.

**Video Walkthrough / Setup / Code Breakdown**

https://www.youtube.com/watch?v=Emypa7YLAhI

Please like/subscribe on YouTube and leave a like on pub.dev to support me!

**Usage**
```
final usersIgMedia = await Navigator.push(context,
   MaterialPageRoute(builder: (context) => 
      InstagramMedia(
         mediaTypes: 0, //choose what to return (see parameters below)
         appID: '70000000000', //app ID for your IG app in your FB Developer Account
         appSecret: '3750x0x0x0x0x0x0x0x0x0x00x0x') //the secret for the app ID
   )
);

print(usersIgMedia[0]); //urls
print(usersIgMedia[1]); //timestamps
print(usersIgMedia[2]); //IDs
print(usersIgMedia[3]); //types (IMAGE, VIDEO, or CAROUSEL_ALBUM)
print(usersIgMedia[4]); //captions
```

**mediaTypes Options**
```
0 - images only (No CAROUSEL_ALBUM)
1 - videos only (No CAROUSEL_ALBUM)
2 - images and videos (No CAROUSEL_ALBUM)
3 - everything - everything (CAROUSEL_ALBUM, VIDEO, IMAGE)
```