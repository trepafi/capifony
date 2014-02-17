Capifony Lt way
===============

- Should have installed capistrano_rsync_with_remote_cache-2.4.0.gem:

  `sudo gem install capistrano_rsync_with_remote_cache`

- I've updated the file `/lib/symfony.rb` adding new variable called `release_subfolder` 

  The reason to do that, is I currently have the symfony2 project as a subfolder in the git repo, so, when capifony executes the git clone, all the action should run under this folder
  
  `run "#{try_sudo} sh -c 'cd #{latest_release}#{release_subfolder} && SYMFONY_ENV=#{symfony_env_prod} #{composer_bin} update #{options}'"`

- To install the custom version of capifony, do:

  `gem build capifony.gemspec`

  `sudo gem install capifony-{version}.dev.gem`

