
 ``` 
# How to Copy Data Automatically From USB to Your PC On Insert
 
Do you want to save time and hassle by copying data from your USB drive to your PC automatically whenever you plug it in? In this article, you will learn how to set up a simple script that will do just that. You will also learn how to customize the script to suit your needs and preferences.
 ![USB cable](https://cdn.pixabay.com/photo/2016/11/22/23/40/cable-1851214_1280.jpg) 
## Why Copy Data Automatically From USB to Your PC On Insert?
 
There are many reasons why you might want to copy data automatically from your USB drive to your PC on insert. For example, you might want to:
 
**Download ★★★★★ [https://t.co/I1tE1TtDDe](https://t.co/I1tE1TtDDe)**


 
- Back up your important files and documents
- Transfer photos and videos from your camera or phone
- Share files with other devices or users
- Sync data between multiple USB drives
- Free up space on your USB drive

Whatever your reason, copying data automatically from your USB drive to your PC on insert can save you time and effort. You don't have to manually open the USB drive, select the files, copy them, and paste them to the destination folder. You can also avoid forgetting or losing your USB drive by having a backup copy on your PC.
 
## How to Copy Data Automatically From USB to Your PC On Insert?
 
To copy data automatically from your USB drive to your PC on insert, you will need to create a simple script using Windows PowerShell. PowerShell is a command-line tool that allows you to perform various tasks on your computer. You can use it to create scripts that automate repetitive or complex actions.
 
Here are the steps to create and run the script:

1. Create a folder on your PC where you want to copy the data from your USB drive. For example, you can create a folder called "USB Backup" on your desktop.
2. Open Notepad and paste the following code into it:

        $source = Get-WmiObject Win32_Volume | ?  $_.Label -eq 'USB'  | select -ExpandProperty Name
        $destination = "C:\Users\YourName\Desktop\USB Backup"
        if ($source) 
          Copy-Item -Path $source\* -Destination $destination -Recurse -Force

This code will copy all the files and folders from the USB drive with the label "USB" to the destination folder on your PC. You can change the label and the destination folder according to your preferences.
3. Save the file as "Copy-USB.ps1" in the same folder where you want to copy the data from your USB drive.
4. Open PowerShell as an administrator by right-clicking on the Start menu and selecting "Windows PowerShell (Admin)".
5. Type or paste the following command into PowerShell and press Enter:

        Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

This command will allow you to run scripts that you have created on your computer.
6. Type or paste the following command into PowerShell and press Enter:

        Register-WmiEvent -Class win32_VolumeChangeEvent -SourceIdentifier volumeChange

This command will register an event that will trigger whenever a volume change occurs on your computer, such as inserting or removing a USB drive.
7. Type or paste the following command into PowerShell and press Enter:

        Action  Invoke-Expression "C:\Users\YourName\Desktop\USB Backup\Copy-USB.ps1"  | Register-ObjectEvent -SourceIdentifier volumeChange -EventName Action

This command will create an action that will run the script that you have created whenever the event that you have registered occurs.
8. You are done! Now, whenever you insert a USB drive with the label "USB" into your computer, it will automatically copy all the data from it to the destination folder on your PC.

## Tips and Tricks 8cf37b1e13


