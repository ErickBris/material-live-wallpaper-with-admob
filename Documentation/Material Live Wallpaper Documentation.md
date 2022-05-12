# Material Live Wallpaper Documentation
Here is the full documentation of this project. Hopefully you can create your own life wallpaper with the easiest way

## Project Structure
![Project structure](https://i.imgur.com/SOEJpFZ.png)

## Dependencies
This project using these libraries bellow to help the app work better.
 - Firebase analytic
 - Firebase Admob
 - Glide
 - Annimon Stream

## Change Live Wallpaper Content
Here is the funny thing about this project, you just have to change only one file, so you got your fully customized app. All you do is just go to **MasterData.java**  file (stored at *data* folder). This file contains all data that you  have to change. 

***Where I have to put my Gif File?*** 
You have to put it at asset folder

**And then, where the code that I have to change?**
Like I said, you have to change it at *MasterData.java* file (find method *getWallpapers()*), heres the snippet code :
```
 public List<Wallpaper> getWallpapers(){
        return new ArrayList<>(Arrays.asList(
                // Category Name, Thumbnail for category, Gif File
                new Wallpaper("Romance", R.drawable.romance, "rain.gif"),
                new Wallpaper("Romance", R.drawable.nature, "bmw.gif"),
                ..............
        ));
    }
```
Wallpaper is the class which it's constructor has 3 parameter :
1. Category name
2. Image for category (put it on drawable folder)
3. Gif file name (put it on asset folder)
 
**How about admob unit ID, do I have to change code at MasterData.java file too?**
Yes, exactly
Go to MasterData.java file and find these codes :
```
public static final String ADMOB_APP_ID = "ca-app-pub-3940256099942544~3347511713";
public static final String BANNER_AD_ID = "ca-app-pub-3940256099942544/6300978111";
public static final String INTERSTIAL_AD_ID = "ca-app-pub-3940256099942544/1033173712";
```
Please check the link below to get more about admob and firebase
https://www.youtube.com/watch?v=9qCxo0D-Sak

**This app contain About menu, where do I have to change the content?**
Some answer, at MasterData.java to
Look up into *getAbout()* method
```
public List<About> getAbout(){
    return new ArrayList<>(Arrays.asList(
            new About("App Name", "Material Live Wallpaper"),
            new About("Version", BuildConfig.VERSION_NAME),
            new About("Developer", "Annas BlackHat"),
            new About("Email", "annas@gmail.com", About.Type.EMAIL),
            new About("Website", "http://annasblackhat.com", About.Type.URL),
            new About("Contact", "+6285720085992", About.Type.PHONE)
    ));
}
```
*About* is a class which has 2 type of constructor
1. With two parameters
   - Title
   - Content
2. With three parameters
   - Title
   - Content
   - Content Type (The app only provides 3 types of content : Url, Phone, Email. if you set the type to Url, its mean, when user click the content, the app will redirect user to browser)
    
## How about firebase analytic?
In this case you have to go to [firebase console](https://console.firebase.google.com) and then create you project. So then, create android app on that, after all finish you will get json file ( *google-services.json* ) that contains all firebase information, put that on app folder.
To get more information about firebase, click link below :
https://www.youtube.com/watch?v=cNPCgJW8c-E

Thanks....
