# Whisky v2.2.4

> NOTE: For the current Version of Whisky, you don't need the following steps!

Whisky is not supported in older Versions, even thou some Games only work with them.

Download and install Whisky here: [Whisky v2.2.4](https://github.com/Whisky-App/Whisky/releases/tag/v2.2.4)

Open Whisky, click install and it will instantly finish with installing GPTK (as it just skips this step). However, some folders got created in this step that we will use later on. Close Whisky after this again.

Download the needed Library.zip file from [here](https://web.archive.org/web/20240416174812if_/https://data.getwhisky.app/Libraries.zip)

Unpack the .zip file with

    unzip Libraries.zip

This will result in a Library.tar.gz file. This needs to be unpacked into the Library Folder inside `~/Library/Application\ Support/com.isaacmarovitz.Whisky`. So use

    cd ~/Library/Application\ Support/com.isaacmarovitz.Whisky
    ls -ahl

You should now see a Libraries folder. Use

    tar -xf ~/Downloads/Libraries.tar.gz

to unpack the file in here. Now use

    sudo xattr -r -d com.apple.quarantine .

to tell the OS that this folder is safe to execute.

Done! Open Whisky and it will work!
