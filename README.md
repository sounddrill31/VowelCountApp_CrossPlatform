# Vowel Count App

Simple C# App built using Avalonia UI. It checks the letters in the string entered and sees how many vowels are present(AEIOUaeiou)

![Screenshot of App](https://github.com/user-attachments/assets/ded065ba-371b-4549-8b2e-a9936330160c)


## Install
- Go to [Releases](https://github.com/sounddrill31/VowelCountApp_CrossPlatform/releases/latest)
- Click on the zip file for the OS you're using(VowelCountApp-ubuntu-latest.zip for 64bit Linux, VowelCountApp-windows-latest.zip for 64bit Windows)

## Building
- Git clone and Enter the folder
  ```bash
  git clone https://github.com/sounddrill31/VowelCountApp_CrossPlatform;
  cd VowelCountApp_CrossPlatform
  ```
- Set up a .NET 8.0 Environment using the [install script](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-install-script).
- Run the restore command to install deps quickly:
  ```bash
  dotnet workload restore
  ```
- Compile the Program
  ```bash
  dotnet build VowelCountApp/VowelCountApp.Desktop --configuration Release 
  ```
- Package the Program
  ```bash
  dotnet publish VowelCountApp/VowelCountApp.Desktop --configuration Release --output ./output
  ```
- Retrieve the Built Files from the output folder

## Known Issues
- On (x)Wayland, the blur is broken and X11 is untested. The AvaloniaUI Media Player App guide says this about the blur stuff:
  > Note, Linux users can not yet take advantage of this due to limitations of X11. The code will run and the window will still work on Linux, but the full effect will not be realised.
- No Native Wayland support is available
- Mac, Android, iOS, Web support is broken/untested
## Credits
- Dan Walmsley for the [Music Store App Guide](https://docs.avaloniaui.net/docs/0.10.x/tutorials/music-store-app/)
