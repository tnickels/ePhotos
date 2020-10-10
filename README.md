# ePhotos v1.7
> released 10/10/2020

This script is provided as freeware, but any donations will be greatly appreciated. If you find this software useful please buy me a coffee via
<a href="https://www.buymeacoffee.com/tnickels" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-orange.png" alt="Buy Me A Coffee" width= "217" ></a>
## Introduction

When Apple dropped the built in email photo resizing option to share photos to an email program, it made things cumbersome. Photos now had to be exported to a folder and then manually dragged into the email client. If the overall email size was too large, you have to do it all over again with different settings.  I had tried all the email programs and tested new ones as they were released. None offered the same functionality Apples iPhoto used to have. Apple Mail badly embeds all images inline and although now Postbox has included image resizing, it too is only available for inline images.

So, a couple of years ago I wrote an Applescript to take a selection of photos within Apple Photos; provide a prompt for three different file size options and send the result to Postbox. The script was not thorough, but it worked. Now having recently updated to Mac OS Catalina everything broke. I was forced to rewrite my code to fix my script and make it compatible with the tighter controls of Catalina.

In the rewrite I added functionality, better error handling and expanded the code to also send resized photos to Microsoft Outlook.


## What is ePhotos

This software adds a function severely missing from the Postbox and Microsoft Outlook Apps. It provides the ability to downsize attached images (not inline images) from the Photos App to your email client. Postbox have provided a "sharing extension" that will allow images to be passed onto Postbox from the Apple Photos App, but that is limited to 10 photos and no downsizing functionality

ePhotos is an Applescript to export photos selected within the Apple Photos App and attached them to a new email in Postbox or Outlook. During the process it gives the user the ability to downsize the images more suitable for emailing


## Supported software

The script is compatible with >= Mac OS 10.14

Apple Photos.app

Email Clients:

	Postbox
	
	Microsoft Outlook 365


## Installation

1.	Copy the script to your Scripts folder within your User/Library
2.	At this point you may want to remove any unneeded scripts from this directory
3.	Within “Security and Privacy” pane of “System Preferences” go to the “Privacy” tab
4.	Click the padlock to unlock the security options and click on “Full Disk Access” in the left hand column
5.	Click on the “+” icon, and traverse the folder structure to locate “Image Events” in the “core services” directory. This can be found at
             Macintosh HD/Library/Core Services/Image Events.    
           Where Macintosh HD is the name of your hard drive
6.	Open the application “Script Editor” located within Applications/Utilities folder
7.	Open the preferences and select the “Show Script menu in menu bar”


## How to Use

1.	Open Photos and make sure you are in the “Thumbnail View”. The script only works when in the “Thumbnail View”. 
2.	Select the images you wish to email. There is no limit to the number of photos you can select.
3.	From the Applescript menu bar item on the right hand side of the menu bar, select “ePhotos”
4.	On the scripts’ first run you will be presented with a few extra dialog boxes asking for permission to access System Events,Image Events, Photos, Finder and    
          your email client. You must allow each of the items for the script to work.
5.	The script will then give you the option to cancel, email the original, a large image with a max dimension of 1600px or a medium image with a max dimension 
           of 800px.


## How Does it Work?

The script creates a cache directory called “com.tnickels.EmailPhotosCache” within /Users/Your username/Library/Caches. Within this directory a temporary folder is created each time you call “ePhotos”. The selected photos are then copied into an “original” directory within this cache folder and they are then resized to the remaining two file size options.

It will then obtain the total file size for each option and ask you which one you would like to use. After selecting the file size, a new email is created and the files are attached.

Finally “ePhotos” cleans up after itself. It tests to see if any of the cache folders are more than 24 hours old. If they are, it deletes them and keeps your system tidy.



## Some personal words

Applescript is not the prettiest, but until the email client developers provide a way to expand their software or include image attachment downsizing within their app, this will work.

Speed improvements can be made through shell scripts or even rewriting the whole Applescript as a shell script, but I have no intention in doing that.



This script is provided as freeware, but any donations will be greatly appreciated.
Please buy me a coffee via https://www.buymeacoffee.com/tnickels



## It’s freeware but how do I get a copy of the code

The script is set to read only and contains a lot of code snippets people may find helpful. I have spent a decent amount of time and effort putting this script together. If you would like access to the code so you can use various pieces in your own code or simply expand on what I have done, buy me a few more coffees coffees and I will send you a copy of the code.

If any changes/improvements are made to the script, used in other software in part or whole or the script is used as a basis for other implementations it is a condition of use that you send me a licence free copy of your work.

## Credits
ePhotos uses [SKProgressBar 1.8](http://klieme.com/Downloads/SKProgressBar/SKProgressBar1.8.zip) to provide progress notification. SKProgressBar is written by [Stefen Klieme](http://www.klieme.de/) and support for SKProgressBar can be found [here](https://macscripter.net/viewtopic.php?id=36409)

ePhotos is developed and maintained by [Travis Nickels](https://github.com/tnickels)


Any issues or pull request can be lodged on the [ePhotos github page](https://github.com/tnickels/ePhotos)

Written by Travis Nickels © 2020

All rights reserved.
