------------------------- Expo ------------------------------------------------
exp start jest-haste-map: Watchman crawl failed. Retrying once with node crawler

In Node
```bash
var watchman = require('fb-watchman');
var client = new watchman.Client();
client.capabilityCheck({optional:[], required:['relative_root']},
  function (error, resp) {
    if (error) {
      // error will be an Error object if the watchman service is not
      // installed, or if any of the names listed in the `required`
      // array are not supported by the server
      console.error(error);
    }
    // resp will be an extended version response:
    // {'version': '3.8.0', 'capabilities': {'relative_root': true}}
    console.log(resp);
  });
```
-------------------------------------------------------------------------------
expo Metro Bundler failed to start. (code: ENOSPC)

echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
---------------------------------VSCODE----------------------------------------
set 2 spaces in tabSize

in user settings:
{
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false
}
-------------------------------------------------------------------------------
enable Emmet expansion when press tab

in USER SETTINGS
{
    "emmet.triggerExpansionOnTab": true
}
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
------------------------------Elementary OS-----------------------------------
How to disable desktop switch on fullscreen

gsettings set org.pantheon.desktop.gala.behavior dynamic-workspaces false
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
---------------------------------Rails----------------------------------------
Delete link doesn't work

gem 'coffee-script-source', '1.9.0'

$ bundle install
$ gem update coffee-script-source
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
----------------------------------Java-----------------------------------------
How to set JAVA_HOME for Java?

```bash
update-alternatives --config java
JAVA_HOME=<PATH>
echo $JAVA_HOME
```
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
---------------------------------Node JS---------------------------------------

Error: Node Sass does not yet support your current environment: Linux 64-bit with false
```bash
npm rebuild node-sass
```
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
------------------------------React Native-------------------------------------
Error when running watchman

20:25:43 [exp] jest-haste-map: Watchman crawl failed. Retrying once with node crawler.
20:25:43 [exp]   Usually this happens when watchman isn't running. Create an empty `.watchmanconfig` file in your project's root folder or initialize a git or hg repository in your project.
20:25:43 [exp]   Error: Watchman error: A non-recoverable condition has triggered.  Watchman needs your help!

echo 256 | sudo tee -a /proc/sys/fs/inotify/max_user_instances
echo 32768 | sudo tee -a /proc/sys/fs/inotify/max_queued_events
echo 65536 | sudo tee -a /proc/sys/fs/inotify/max_user_watches
watchman shutdown-server
-------------------------------------------------------------------------------
windows android unable to load script from assets...

1. (in project directory) mkdir android/app/src/main/assets
2. react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
3. react-native run-android

You can automate the above steps by placing them in scripts part of package.json like this:

"android-linux": "react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res && react-native run-android"

Then you can just execute npm run android-linux from your command line every time.

-------------------------------------------------------------------------------

Error:
module hmrclient is not a registered callable module

Solution:
Go to the android/ directory of your react-native project
Create a file called local.properties with this line:

```bash
sdk.dir = /Users/USERNAME/Library/Android/sdk
```

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------

#Git
- to change number of seconds to cache credentials use timeout parameter (30 minutes in this example):
```bash
$ git config credential.helper 'cache --timeout=1800'
```
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
#Atom

Atom autocomplete HTML tags in JSX files
in keymap.cson add
```
'atom-text-editor[data-grammar="source js jsx"]:not([mini])':
  'tab': 'emmet:expand-abbreviation-with-tab'
```
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
# RVM

-PATH is not properly set up

Warning! PATH is not properly set up, '/home/lecco/.rvm/gems/ruby-2.3.0/bin' is not available,
         usually this is caused by shell initialization files - check them for 'PATH=...' entries,
         it might also help to re-add RVM to your dotfiles: 'rvm get stable --auto-dotfiles',
         to fix temporarily in this shell session run: 'rvm use ruby-2.3.0'.

```bash
PATH="$GEM_HOME/bin:$HOME/.rvm/bin:$PATH" # Add RVM to PATH for scripting
[ -s ${HOME}/.rvm/scripts/rvm ] && source ${HOME}/.rvm/scripts/rvm
```
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
# RAILS

/home/lecco/Dropbox/rails/blog/bin/spring:11:in `<top (required)>': undefined method `path_separator' for Gem:Module (NoMethodError)
	from bin/rails:3:in `load'
	from bin/rails:3:in `<main>'

gem pristine --all 
-------------------------------------------------------------------------------
RAILS

/home/lecco/.rvm/gems/ruby-2.2.2/bin/rake:22:in `<main>': undefined method `activate_bin_path' for Gem:Module (NoMethodError)

bundle exec rake db:migrate --trace
-------------------------------------------------------------------------------
playon commit

ssh-add ~/Main/pilgrim
git pull --rebase

git add ARCHIVOS
git commit -m "[BRANCH TRABAJADO]commit"
git push
-------------------------------------------------------------------------------
Update nodejs:

downgrade node to 0.10.36
  sudo npm cache clean -f
  sudo npm install -g n
  sudo n 0.10.36

upgrade node to stable v
  sudo npm cache clean -f
  sudo npm install -g n
  sudo n stable

-------------------------------------------------------------------------------
Unrecognized VM option 'MaxPermSize=350m'
Error: Could not create the Java Virtual Machine.
Error: A fatal exception has occurred. Program will exit.

i solved the problem changing the JAVA_HOME value to:
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_60
and i added it to /etc/environment file.
-------------------------------------------------------------------------------
-react native could not connect to development server android

Delete the App from your phone! I tried several steps, but that did it eventually.

1- If you tried to run your app before but failed, delete it from your android device.
2- Run $ react-native run-android
3- Open the React Rage Shake Menu from within your app on your android device, go to Dev Settings and then to Debug server host & port for device. There enter your server IP (IP of your computer) and host 8081, e.g. 192.168.50.35:8081. On a mac you can find the IP of your computer at System Preferences -> Network -> Advanced... -> TCP/IP -> IPv4 Address.
4- Open the Rage Shake Menu again and click Reload JS.


-------------------------------------------------------------------------------
create a program launcher

sudo nano /usr/share/applications/PROGRAM.desktop

[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Exec="/home/username/Programs/AndroidStudio/bin/studio.sh" %f
Icon=/home/username/Programs/AndroidStudio/bin/idea.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=jetbrains-android-studio
Name[en_GB]=android-studio.desktop
-------------------------------------------------------------------------------
ZSH theme robbyrussell

curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
-------------------------------------------------------------------------------
“shake” an Android emulator

adb shell input keyevent KEYCODE_MENU
-------------------------------------------------------------------------------
Freya - HOW TO FIX INVISIBLE MOUSE CURSOR ISSUE IN eOS freya

gsettings set org.gnome.settings-daemon.plugins.cursor active true
-------------------------------------------------------------------------------
Freya - problema doble cursor

gsettings set org.gnome.settings-daemon.plugins.cursor active false
-------------------------------------------------------------------------------
Montar particion de windows suspendida

sudo ntfsfix /dev/sda1
-------------------------------------------------------------------------------
Evitar que git solicite usuario y contraseña cada vez

git config --global credential.helper 'cache --timeout=3600'
-------------------------------------------------------------------------------
Open folder from terminal

xdg-open .
-------------------------------------------------------------------------------
Create a Desktop Shortcut on GNOME Desktop

sudo apt-get install --no-install-recommends gnome-panel 
sudo gnome-desktop-item-edit /usr/share/applications --create-new 
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
#Linux
-------------------------------------------------------------------------------
install boot-repair

sudo apt-get install software-properties-common python-software-properties
sudo add-apt-repository ppa:yannubuntu/boot-repair
sudo apt-get update
sudo apt-get install boot-repair

-------------------------------------------------------------------------------

GRUB does not detect Windows:

1) Boot Ubuntu and mount your Windows partition (simply open the disk on Nautilus)
2)Run the following on the command line (Ctrl+Alt+t):
$ sudo os-prober
3) If your Windows installation was found, you can run:
$ sudo update-grub

-------------------------------------------------------------------------------

-create iso image
```bash
dd if=/dev/cdrom of=/home/lecco/cdrom_image.iso
```
-------------------------------------------------------------------------------
- Unable to mount Windows (NTFS) filesystem due to hibernation

```bash
sudo ntfsfix /dev/sdXXXXX
```
-------------------------------------------------------------------------------
Run a COMMAND every hour

```bash
watch --interval=3600 [COMMAND]
```
-------------------------------------------------------------------------------
Know my global IP

curl ipinfo.io
-------------------------------------------------------------------------------
¿Cómo ejecutar comando del terminal al iniciar nuestro Linux?

```bash
sudo nano /etc/rc.local
```
y agregar el COMMANDO a ejecutar

-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
#Offimatica

-contar palabras en una celda
=IF(LEN(TRIM(A1))=0;0;LEN(TRIM(A1))-LEN(SUBSTITUTE(A1;" ";""))+1)
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
