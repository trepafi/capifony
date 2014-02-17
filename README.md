Capifony Lt way

- Should have installed capistrano_rsync_with_remote_cache-2.4.0.gem:
  sudo gem install capistrano_rsync_with_remote_cache

- I've updated the file /lib/symfony.rb adding new variable called release_subfolder for when I have the root of the symfony project in a subfolder instead of the root one
  run "#{try_sudo} sh -c 'cd #{latest_release}#{release_subfolder} && SYMFONY_ENV=#{symfony_env_prod} #{composer_bin} update #{options}'"
