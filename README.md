# openinno's drupal starter kit
Hello and welcome! This is the Openinnovations Drupal installation and or starting kit.

## First things first
Make sure that you have installed lando and docker on your computer, Windows machines are not recommended.

About docker, you can have some information [here](https://docs.docker.com/engine/install/) or then again [here](https://docs.docker.com/engine/install/debian/) .

For Lando, the documentation has been changed, but basically what you need to do is to go [here](https://github.com/lando/lando/releases) and download this [file](https://github.com/lando/lando/releases/download/v3.21.0-beta.11/lando-x64-v3.21.0-beta.11.deb), so you get the latest version of Lando. 

### What to do next
Clone the project on your local, run this command on your termimal, git clone git@github.com:n00bsaiboth/openinno-drupal-starter-kit.git . 

Then, when you get docker and lando up and running, you need to give it the following commands, 

lando start

lando composer install

lando db-import <from the sql folder>

