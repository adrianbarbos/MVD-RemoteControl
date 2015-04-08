# MVD-RemoteControl

######Ca sa ne fie mai usor de lucrat cu MVD care nu are screen, putem folosi acest tool.

The tool does the following:

Repeatedly grab a screenshot from the phone and display it in a Window
Capture keyboard events and forward them to the phone
Capture mouse clicks and drags and forward them to the phone
It’s slow as hell (everything is being done through shell calls, which makes the screenshot updates particularly slow), but it works.

Before you first start it, make sure you have adb installed and modify the config file provided with the download. It contains four settings:

adbCommand – the full path to the adb tool as a shell command. Linux users note that Java doesn’t seem like the ~ character in file paths to access the home directory.
screenshotDelay – the delay (in milliseconds) between displaying a screenshot and grabbing the next one. Note that the actual grabbing process will probably take considerably longer than this delay, so the update rate will be slower.
localImageFilePath – the tool has to download the image file from the phone. This path tells it where to store the file on the local system before displaying it.
phoneImageFilePath – the location on the phone where the screenshot file is stored before downloading it.
Once the configuration is done, simply run the tool like this:

java -jar adbcontrol.jar
If you put the config file in a different directory, you can add the path to it as an option after the jar file name.
