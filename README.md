pushmenu
=============

Push notifications from you Mac to your iOS device via Prowl, Notifo or Boxcar. 

pushmenu is a small menu bar application that sends the content of you clipboard as 
push notification to you iOS device. 

Features:

* Pushes clipboard content 
* Provides system service to push any selected text without copying to the clipboard first
* Keyboard shortcut
* AppleScript Support (e.g. for Automator support)
* Credentials are stored in system keychain
* Automatic updates via Sparkle
* Growl support


![pushmenu](https://github.com/kalcher/pushmenu/raw/master/pushmenu/screenshot.png)

AppleScript
------------
The AppleScript interface to pushmenu currently consists of one command with one parameter:

*sendmessage text : a text parameter passed to pushmenu*

The message is pushed out to all active services.

#### Example (push.scpt):

    on run {input}
	    tell application "pushmenu"
		    sendmessage input
	    end tell
    end run


Terminal
-----------
The AppleScript interface can also be used to provide terminal access to pushmenu. You need to have the above script (push.scpt) compiled and saved.

#### Example:
Run in Terminal:

    osascript /path/to/push.scpt "Hello World"