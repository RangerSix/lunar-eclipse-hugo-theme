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
cd to that folder. There should be a few folders there but we will only be using the theme folder and the hugo.toml file.

 
