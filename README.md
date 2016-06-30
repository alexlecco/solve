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
-------------------------------------------------------------------------------
-------------------------------------------------------------------------------
