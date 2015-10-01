# MacLockDesktop
This project is used to lock the desktop image of an Apple computer. 

## Support OSes
Tested with Mac OS X 10.9 and 10.10

#How-to
1. Determine the image you want
2. copy that image to `/Library/Desktop Pictures`
3. Right click the image and `Set Desktop Picture`
3. Copy com.stackexchange.apple.65938.plist to `/Library/LaunchAgents/`
4. Open the plist with your choice of app. (Textwangler, xcode, etc)
5. Replace `youPictureFile.jpg` with the file name of picture.
6. Don't forget to save.
7. Run the two commands in the `commands` file. (sudo is required) No restart is needed.

