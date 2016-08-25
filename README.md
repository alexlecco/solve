-------------------------------------------------------------------------------
RVM

-PATH is not properly set up

Warning! PATH is not properly set up, '/home/lecco/.rvm/gems/ruby-2.3.0/bin' is not available,
         usually this is caused by shell initialization files - check them for 'PATH=...' entries,
         it might also help to re-add RVM to your dotfiles: 'rvm get stable --auto-dotfiles',
         to fix temporarily in this shell session run: 'rvm use ruby-2.3.0'.


PATH="$GEM_HOME/bin:$HOME/.rvm/bin:$PATH" # Add RVM to PATH for scripting
[ -s ${HOME}/.rvm/scripts/rvm ] && source ${HOME}/.rvm/scripts/rvm
-------------------------------------------------------------------------------
RAILS

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
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
