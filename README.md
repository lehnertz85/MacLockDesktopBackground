# MacLockDesktop
This project is used to lock the desktop image of an Apple computer.

I have searched the webs to find the best method to lock down the background on Macs and this is the best. I origionally discovered this when 10.9 first came out and the origional source can be found [here](http://apple.stackexchange.com/questions/65938/how-to-restrict-changing-desktop-wallpaper).

When a user attemps to change the desktop picture, it will let them, but it will get reverted back to the original after a few seconds.

This method also prevents users from right clicking in safari to change the background. 

I'm not sure if there's any performance issues with this method, so use with caution.

## Supported OSes
Tested with Mac OS X 10.9 and 10.10

#How-to
1. Determine the image you want
2. copy that image to `/Library/Desktop Pictures`
3. Right click the image and `Set Desktop Picture`
3. Copy com.stackexchange.apple.65938.plist to `/Library/LaunchAgents/`
4. Open the plist with your choice of app. (Textwangler, xcode, etc)
5. Replace `yourPictureFile.jpg` with the file name of picture.
6. Don't forget to save.
7. Run the two commands in the `commands` file. (sudo is required) No restart is needed.

# The Commmands
**sudo chown root /Library/LaunchAgents/com.stackexchange.apple.65938.plist**
Sets the plist permission to root, so no user can edit them.

**sudo launchctl load /Library/LaunchAgents/com.stackexchange.apple.65938.plist**
Has launchctl load the plist so it's listening.


