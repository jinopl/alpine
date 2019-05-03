# Read Me!

This is a **Alpine lamp** **docker** project . it can be used for testing purpose , Not recommended for production .

check build status below 

[![Build Status](https://travis-ci.org/jinopl/alpine-lamp.svg?branch=master)](https://travis-ci.org/jinopl/alpine-lamp)


# Steps
		

 - Clone this project
 - If the project require composer Edit docker-entrypoint.sh and uncomment #composer_location and add location
 - Build the project using " docker build -t docktemp . "
 - Run the container <br> docker run --rm -v "$(pwd)\"/html:/var/www/localhost/htdocs/ -e MYSQL_ROOT_PASSWORD=qwerty -p 8012:80 -p 3366:3306 --name "project_name" docktemp
 - project can be accessed via localhost:8012
 
 # Note
 
 - Document root in this container **/var/www/localhost/htdocs/**
 - please Put all HTML files inside HTML folder.
 - MySQL root password **qwerty** and it can be changed by editing in docker-entry.sh
 - MySQL can be manged through adminer software , it's already in the container can be accessed by [link here](localhost:8012/adminer.php)
 
 - Installed software's


> Apache 2 <br>
> PHP 7.2 <br>
> Maria db <br>
> Composer
