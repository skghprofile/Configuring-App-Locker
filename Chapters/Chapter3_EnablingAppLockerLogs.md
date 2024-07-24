# Chapter 3 - Enabling AppLocker Logs

## Introduction 

Now that AppLocker is enabled but in Auditing mode, I need to be able to see what triggered an AppLocker rule and when it happened. This is easily done by looking at the logs AppLocker generates in Windows Event Viewer.

## Creating AppLocker Event Viewer Custom View

Like in Chapter 1, AppLocker is buried deep within several submenus in the Group Policy Editor. This is also the case with Windows Event Viewer. A quick and easy way to access the AppLocker logs in Event Viewer is to create a custom view, which I will demonstrate below.

To start, click on the Windows Search box in the bottom left of the Windows PC search for "event viewer", and click on the "Event Viewer" result with the notebook icon that should be the best result.

![Event Viewer Windows Search Box](/Images/AL-img17.png)

To create the Custom View now that the Windows Event Viewer window is open, right-click the "Custom Views" folder near the top left of the window and then left-click the "Create Custom View..." button in the context menu to open the "Create Custom View" window.

![Windows Event Viewer](/Images/AL-img18.png)

In the "Create Custom View" window, left-click the dropdown button in the same line as "Event Logs" to open the menu and select which logs will be used for this new Custom View.

To only select the AppLocker logs without selecting all the other logs, navigate through the path below and only enable the checkbox labeled "AppLocker".

AppLocker Log Path: **Applications and Services Logs > Microsoft > Windows > AppLocker**

This should only enable the logs for AppLocker for this Custom View and also the sub-log categories for AppLocker, as shown in the images below:

![Create Custom View window](/Images/AL-img19.png)
![Create Custom View window](/Images/AL-img20.png)

To finish creating the new custom view, I clicked the "OK" button near the bottom right corner of the "Create Custom View" window. 

![Create Custom View window](/Images/AL-img21.png)

After clicking "OK", I'm now in the "Save Filter to Custom View" window. Here, I changed the name of the new custom view to "AppLocker" and then clicked the "OK" button on the right side of the window to finish creating the custom view.

![Save Filter to Custom View window](/Images/AL-img22.png)

I can verify that the custom view was successfully created by seeing it as a new filter in the "Custom View" folder near the top left of the Event Viewer main window.

![Windows Event Viewer Custom View](/Images/AL-img23.png)

## Next Chapter: 
### [Chapter 4 - Importing AppLocker Rules](/Chapters/Chapter4_ImportingAppLockerRules.md)
