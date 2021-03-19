#Composer Install Error on - Kylekatarnls package updater
In some Laravel projects when you want to do a ```composer install``` or ```composer update``` there is an error about kylekatarnls package.

When this happens 2 things may be at fault:
1. PHP version does not meet the requirements
2. Composer version is incompatible with the current php version

How to deal with this:
1. ensure that it's using PHP7.2 or the relevant version.
2. You may have to upgrade or downgrade to the relevant Composer version
	- you can do this by running composer self-update -1 (tells it to get version 1 because version 2 is the one causing the problem - incompatible)
3. After that run ```composer install --no-plugins```
4. Then run ```composer dumpautoload -o```

The lazy alternative:
1. Download the appropriate version of Composer for your version of PHP and Laravel from https://getcomposer.org/download/
2. The file will be a composer.phar
3. Place this in the main directory of your project
4. You will make use of this by running ```php composer.phar install``` etc
