Want to leave a suggestion or even contribute? Yes, Please. Any help will be greatly appreciated.
Besides I need all the help I can get.lol. Thank You!

Welcome.
You probably are saying why do it this way? I can use a ready made theme or even use AI to make a theme.
This is true, but if you use a ready made theme, it want be yours and you will probably have to sacrifice something you want in your theme.
Using AI, I find is never right. Spent more time with errors than blogging. 
This way you get to build the house the way you want it, I'm just giving you the foundation.
And perhaps we both can learn something. lol..

Build Environment:

I use Windows 11. So that is what these instructions are for.

1. Windows PowerShell.
2. Windows Visual Studio Code or VS Code (you can get from windows store).
3. Git for windows. I would use this link because you get a more robust version.
              https://gitforwindows.org
4. Go, program language. get it from here  
              https://go.dev/doc/install
5. Hugo, go here https://github.com/gohugoio/hugo/releases/tag/v0.145.0 and you want to download
   hugo_extended_0.145.0_windows-amd64.zip. This is the lates version as of writing this.
   To keep this short as possible not going to give instructions on how to install. 

Ok, now we should have everything we need to build and customize a hugo blog/website.
Lets make sure.

open powershell and type

  git version
(this should give a git version number with on errors)

  go version

  hugo version

No errors? 
Lets begin!

1. Create a new hugo site. Still in powershell cd to a folder where you want your site to be. I would suggest NOT putting it in a onedrive folder.
You could create a new folder in your dir, something like myhugosite. cd to you new dir, it should be empty.
Now create your new site with the command

   hugo new site yoursitename  (replace yoursitename with what you want call your site)
   
then hit enter and you should now have a new folder with your site name.
cd to that folder. There should be a few folders there but we will only be using the theme folder and the hugo.toml file (for now anyway).

  ..Installing the theme..

There are two ways to do this. 

1. Simply download the zip from the green code button. Should save in downloads folder or wherever you save downloaded file.
   Extract the zip. You should now have a folder called, lunar-eclipse-hugo-theme-main. Open that folder and you should have another folder with the same name, rename that folder to lunar-eclipse.
   Once renamed make sure inside the lunar-elcipse folder you have the theme.toml, config.toml,README.md and two folders, static and layouts.
Now you can copy or move lunar-eclipse folder to the themes folder in your hugo site that you built.

2. Download the theme as a Submodule. To do it this way, in powershell make sure you are in the root of your hugo site. Then use this command to install the theme.
       
git submodule add https://github.com/RangerSix/lunar-eclipse-hugo-theme.git themes/lunar-eclipse

Now your theme is installed.

  ..Lets do a quick test..

Again in the root of your hugo site in powershell run this command

hugo server -t lunar-eclipse

FYI. The -t tells hugo to use the theme

No errors?! yahoo!

This will build your site with basic lunar-eclipse theme. It should have the site local so you can view it.
Open your browser and type localHost:1313 in the address field it should open your new site with the basic lunar-eclipse theme.
Make sure to Ctrl+c to stop the local server when your done.

...Now lets add a post...

Back in powershell at the root of your site type

hugo new posts/postname.md  (replacing postname with the name you want for your post).

hit enter it should create a file in content\posts\postname.md.
Using file explorer open that file with VS code. You should see the front matter at the top.
Here you will need to change draft = true to draft = false. Otherwise hugo will not add it to the site.
Also change the title to what ever you want to call your post.
Now tab down and write your post. When done save the file and return to the root of your site folder.

...Lets test to see if your post shows now...

In the root of your site folder there is a file called hugo.toml.
We are going to edit this file so hugo will use the theme without telling it to every time.
In file explorer right click and choose open with VS code. All you need to do is add
theme = "lunar-eclipse"  make sure to space before and after =.
While your here you change title = "to what you want to name your site".
Save and close.

Now back in powershell in the root of your site type 

hugo  (this will build site with your new post)

then all we have to do is type

hugo server (this will load the site where you can see your post like before at localHost:1313)

Did your new post show? yahoo..
Now close the server back at powershell by pressing Ctrl+c.

...Now lets make it your own...

Using file explorer go to your site.
Open the themes folder and then open lunar-eclipse folder. Now open static and then css folders.
In the css folder there is a file called styles.css. Open that file with VS code. 
This is where you can make changes to your site as you wish. You can change colors for everything here.
VS code makes it easy. Make the changes you want save file then check out your changes with hugo server.

At this point I am going to end this. But you can use AI to add many features. Just make sure to let AI know
you are using hugo.

HAPPY CODING!!



 
