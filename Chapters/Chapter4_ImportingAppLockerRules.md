# Chapter 4 - Importing AppLocker Policies

## Introduction

In this chapter, I will import ThioJoe's policies as a baseline for my AppLocker configuration from his YouTube video description.

## Downloading and Importing the Rules

From ThioJoe's YouTube video, in the description, there is a download link to a Google Drive folder in which he exported a version of his own AppLocker policies for others to use as a baseline and to configure further to fit each user's needs.

To download the rules, I started by clicking on the [Google Drive download link](https://drive.google.com/file/d/1RwZJeYjuvaY-xvF1zhEWT8WHrfOs0Jaz/view) in the YouTube video's description:

![YouTube Video Description](/Images/AL-img24.png)

I then clicked the download icon to download the whole folder as a .zip file:

![Google Drive Folder](/Images/AL-img25.png)

After downloading the "ThioJoe AppLocker Resources - v6" .zip file, I unzipped the file and navigated to the "AppLocker Policies" folder inside where the "AppLocker Policy - Thio Starter Policy + MS Recommended Blocks.xml" file is located.

Relevant File Path: **ThioJoe AppLocker Resources - v6 > AppLocker Policies**

![AppLocker Resources Download](/Images/AL-img26.png)
![AppLocker Rule/Policy File](/Images/AL-img27.png)

Back in the AppLocker settings window in the Group Policy Editor (Accessed by the AppLockerSnapIn shortcut created in Chapter 1), I right-clicked the AppLocker text and clicked "Import Policy..." in the context menu.

![AppLocker Settings/Configuration Window](/Images/AL-img28.png)

In the "Import Policy" window, I navigated to where the unzipped "AppLocker Policy - Thio Starter Policy + MS Recommended Blocks.xml" file was located, clicked it to select the .xml file, and then clicked the "Open" button near the bottom right of the window to import the .xml policies.

Note: I moved the "ThioJoe AppLocker Resources - v6" .zip file from my downloads folder into a new folder on my Desktop named "AppLockerZip" and unzipped the file in there. This is why my path to the .xml file location differs from just doing all the steps above in the Downloads folder.

![Import Policy Window](/Images/AL-img29.png)

Before the policy was successfully imported, I clicked the "Yes" button on the warning popup window, which explained that importing this .xml file would overwrite all existing policy rules.

![Import Policy Warning Window](/Images/AL-img30.png)

After clicking yes, I see that 0 rules were removed and 59 rules were imported.

![AppLocker Import Successful Window](/Images/AL-img31.png)

To verify that the rules were created successfully and can be edited, I re-opened the "AppLockerSnapIn.msc" shortcut that was created on my desktop since it was closed automatically after the import.

On the main AppLocker settings page, I can see that under the "Overview" panel, there are:
- 44 Executable Rules
- 1 Windows Installer Rules
- 3 Script Rules
- 1 Packaged App Rules
- 10 DLL Rules

![AppLocker Main Settings Window](/Images/AL-img32.png)

A quick check cycling through the AppLocker rules menus on the left shows that they are imported and can be edited further:

![AppLocker Executable Rules Window](/Images/AL-img33.png)
![AppLocker Windows Installer Rules Window](/Images/AL-img34.png)
![AppLocker Script Rules Window](/Images/AL-img35.png)
![AppLocker DLL Rules Window](/Images/AL-img36.png)
![AppLocker Packaged App Rules Window](/Images/AL-img37.png)

## Next Chapter: 
### [Chapter 5 - Additional Configurations](/Chapters/Chapter5_AdditionalConfigurations.md)
