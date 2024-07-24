# Chapter 2 - Enabling AppLocker

## Introduction 

In this chapter, I will be enabling AppLocker in auditing mode. When the AppLocker rules are enabled in auditing mode, they will be logged but not actually block the execution if a rule is triggered. Before AppLocker starts to enforce the rules configured, I want to further tweak and configure the rules from the baseline to ensure that regularly known and  trusted executables, installers, scripts, packaged apps, and DLLs are not immediately blocked by AppLocker if they trigger a rule that is initially configured.

## Enabling AppLocker In Auditing Mode

My starting point for this chapter will be the AppLocker main settings/configuration window from the shortcut created in the previous chapter:

![AppLocker Window](/Images/AL-img13.png)

Now I need to navigate to the AppLocker properties menu. To do so, right-click the "AppLocker" text near the top-left of the window and then left click the "Properties" button in the context menu:

![AppLocker Context Menu](/Images/AL-img14.png)

In the AppLocker Properties window, the first thing I want to do is enable the ability to audit and enforce rules for DLLs since by default, they are not enabled. To do this, I switched to the "Advanced" tab at the top of the window, clicked the checkbox to enable "Enable the DLL rule collection" and finally clicked the "Apply" button at the bottom right of the window to apply the changes.

![AppLocker Properties Window](/Images/AL-img15.png)

Now that DLL rules are enabled, I now need to configure AppLocker to enable and audit all the other rules. For this, I switched back to the "Enforcement" tab by clicking it at the top left of the "AppLocker Properties" window and made sure that all of the rules in the "Enforcement" tab were enabled with the "Configured" checkbox. I also changed all of the drop down menus for each of the rules to "Audit only" instead of "Enforce rules". I then clicked the "Apply" button at the bottom right of the window to apply the changes.

![AppLocker Properties Window](/Images/AL-img16.png)

After all of the rules are configured for AppLocker on my PC, I will change all of the dropdown rules in the AppLocker Properties to "Enforce rules" so that AppLocker will block once a rule is triggered.

## Next Chapter: 
### [Chapter 3 - Enabling AppLocker Logs](/Chapters/Chapter3_EnablingAppLockerLogs.md)