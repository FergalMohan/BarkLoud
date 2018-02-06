#Bark Loud Sample App (based on Cloud Kit Messenger)

CloudKitMessenger is a part of [Loose Leaf](https://getlooseleaf.com), and allows for sending text and binary messages between users through CloudKit on iOS. The Sample App has been enhanced to include a  You will need to run
```
pod install
```
from the folder where the Podfile resides to get JSQMessagesViewController from CocoaPods.
N.B. the JSQMessagesViewController pod is no longer being updated and is used just for demo purposes. Let us know if you come across an equivalent (maybe ZHChat ?) that slots in painlessly !

## Building

This workspace contains both the updated CloudKitMessenger and the Simple CloudKit Messenger App..

```
open 'Simple CloudKit Messenger Sample.xcworkspace'
```

##Setup

You'll need to configure your iCloud/CloudKit capabilities. If you are running the sample app, you'll need to use a custom container name.

![iCloud Configuration](http://content.screencast.com/users/sprynmr/folders/Snagit/media/d2ad40e9-0ad4-4fd3-9cd1-931064a2d17a/cloudkit.png)

##Basic Usage

###Login

CloudKit doesn't offer an exact equivalent to logging in. If the user is logged into iCloud on their device, they are logged into iCloud as far as your app is concerned. You need to be logged in to iCloud to be able to find and ohat with friends.


###Friends

The Sample App will list all friends that are also using the App. You can switch between the list of friends and the latest messages by using the Tab Controlbar.

###Fetching messages

Fetching messages is triggered when a friend is selected. All the previous messages will be retrieved and displayed in a JSQMessagesViewController subclass called ChatViewMessenger.

###Sending messages

You can send a message to the friend by typing it into the Input Text field at the bottom of the ChatViewMessenger screen and hitting the "Send" button. When the friend's device receives the remote notification it will automatically add the new chat message to the bottom of the conversation if the ChatViewMessenger is being displayed allowing an Instant Messaging interaction.




