# openinno's drupal starter kit
Hello and welcome! This is the Openinnovations Drupal installation and or starting kit.

## First things first
Make sure that you have installed lando and docker on your computer, Windows machines are not recommended.

About docker, you can have some information [here](https://docs.docker.com/engine/install/) or then again [here](https://docs.docker.com/engine/install/debian/) .

For Lando, the documentation has been changed, but basically what you need to do is to go [here](https://github.com/lando/lando/releases) and download this [file](https://github.com/lando/lando/releases/download/v3.21.0-beta.11/lando-x64-v3.21.0-beta.11.deb), so you get the latest version of Lando. 

### What to do next
Clone the project on your local, run this command on your terminal, `git clone git@github.com:n00bsaiboth/openinno-drupal-starter-kit.git` . 

Then, when you get docker and lando up and running, you need to give it the following commands, 

`lando start`

`lando composer install`

`lando db-import <from the sql folder>`

`lando drush cim -y`

`lando drush cr`

`lando drush updb -y`

`lando drush cr` .

Congratulations, you have a fresh D10 installation to play with.

## Run project on actual LAMP-server

There are few things that you need to consider:
- Make sure that your LAMP-stack is up to date.
- If composer gives you an error, that it can't find some `PHP extensions`, make sure that you have installed them.
- You might need to `unzip` the `database dump`, found in the `/sql` folder, before you import it.
- Change the `database credentials` from the `settings.php` file.

If you think that everything is set and you get an error like this, 
`Composer detected issues in your platform: Your Composer dependencies require a PHP version ">= 8.2.0". `
Try run `composer install` with `--ignore-platform-reqs`.

Also noticed, that the site is giving you a lot of warnings, something like, `Warning: mkdir(): Permission denied in..`, so you might need to create the files folder under `sites/default/` and `chmod` that to `777`.

This is not the bullet proof way to do it, but it's working. You can find the working demo from here, [openinnovations | dev/test](http://openinnovations.ddns.net:2224/). 
