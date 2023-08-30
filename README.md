# MacVM

Virtualizing macOS with Apple Silicon host.

<img width="771" alt="Config" src="https://user-images.githubusercontent.com/1725664/124231369-04456000-dac5-11eb-895c-af933a08a5d7.png">

<img width="769" alt="Install" src="https://user-images.githubusercontent.com/1725664/124231322-f68fda80-dac4-11eb-91b8-e29301f50430.png">

<img width="767" alt="Run" src="https://user-images.githubusercontent.com/1725664/124231661-6dc56e80-dac5-11eb-9fea-b6bcd4fb5db6.png">

## Starting from scratch

1. Download up to date [MacOS ipsw file](https://ipsw.me/product/Mac)
2. Disconnect any external displays.
3. Build and run the `MacVM.xcodeproj` Xcode project
	- In the dialog the opens, click "Create New Document"
	- Adjust VM parameters as needed
	- Save (⌘s or File->Save) with name `MacVM clean.macosvm`
	- Click "Select IPSW and Continue" and select the file you downloaded in step 1.
	- Click "Install"
4. Tap the Play button in the top right corner to launch the Virtual Machine.
5. Setup MacOS to your liking. Stop when you've reached a good rollback point.
	- Make sure to enable File Sharing (System Preferences -> Sharing)
6. Save to the macosvm file again.
7. Continue on to the next section now that you have a rollback point.

## Starting from a rollback point with some basics already configured

1. Duplicate `MacVM clean.macosvm` and rename it `MacVM.macosvm`.
2. Disconnect any external displays.
3. Open and run the `MacVM.xcodeproj` Xcode project.
4. Select the newly created `MacVM.macosvm` when prompted or with File -> Open. 
5. Tap the Play button in the top right corner to launch the Virtual Machine.
6. Password: {whatever you initially setup in the `MacVM clean.macosvm` image}
7. At this point it's ok to reconnect external displays.
8. Open Finder on host machine -> Virtual Machine -> {shared folder name}
	- Upload any necessary files:
		- Current Xcode version downloaded from Apple (zipped)
		- Command Line Tools for Xcode dmg file
		- Environment Setup doc exported to PDF (for easy access to links)
		- notes.txt file with any passwords, api keys, GitHub personal access token, etc.
9. Follow Environment setup doc
