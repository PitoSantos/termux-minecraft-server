# ANDROID MINECRAFT SERVER
> To do this you will need Termux. Open the app and follow the steps below.
## 1. Setting up Ubuntu
- Install Ubuntu by entering this script:
```
pkg install wget openssl-tool proot -y && hash -r && wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh && bash ubuntu.sh
```
- You can run it with the following script:
```
./start-ubuntu.sh
```
> You should be seeing `root@localhost:~#` on the command bar after this.
## 2. Installing Java and others
- In order to install Java, run the following commands one by one:
```
apt-get update
```
```
apt-get install openjdk-17-jre
```
- Also install the file browser: *(to open files use: `nano <filename.extension>`)*
```
apt-get install nano
```
## 3. Installing the server.jar file
- Run the following commands one by one: *(You can change the download URL for the server.jar)*
```
wget -O server.jar https://api.papermc.io/v2/projects/paper/versions/1.20.1/builds/196/downloads/paper-1.20.1-196.jar
```
```
chmod +x server.jar
```
## 4. Setting up the server
- Use this to run the server:
```
java -Xmx1G -Xms1G -jar server.jar nogui
```
- Use the following commands to edit the files:
```
nano eula.txt
```
- To access the files from the file manager:
```
am start -a android.intent.action.VIEW -d "content://com.android.externalstorage.documents/root/primary"
```
> You can also access with [Material Files](https://play.google.com/store/apps/details?id=me.zhanghai.android.files) setting up the external storage.
## 5. Connecting to the server (Playit.GG)
- To install Playit.GG open a new session on Termux (swipe to the left) and start Ubuntu again:
```
./start-ubuntu.sh
```
- Then, once Ubuntu is started, execute the following commands sepparately: *(You will only have to do it once)*
```
wget -O playit https://github.com/playit-cloud/playit-agent/releases/download/v0.15.10/playit-linux-aarch64
```
```
chmod +x playit
```
- Finally to run Playit use this:
```
./playit
```
> To setup Playit.GG just follow the prompts.
## 6. Starting the server regulary
- To start the server use the following in order:
```
./start-ubuntu.sh
```
```
java -Xmx1G -Xms1G -jar server.jar nogui
```
- To start Playit.GG use the following in order: *(Use this in a new session)*
```
./start-ubuntu.sh
```
```
./playit
```
# TERMUX COMMANDS
- Create folder/directory: `mkdir example`
- Access directory: `cd example` *-- cd itself will take you to the main directory*
- Remove/delete: `rm file or rm -r directory`
- Rename: `mv oldname newname` *-- applies to directories too*
