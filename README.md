# Zeus PHP - CakePHP3

CakePHP3.2 ready to use with Zeus.

Zeus is a work in progress for [FreeCodeCamp](http://freecodecamp.com), an opensource learning platform for programmers.

It's goal is to give access to vagrant virtual machines configured for a lot of languages and ready to use with GitHub and Heroku.


## Prerequisites:
  - VirtualBox
  - Vagrant (with utils module)
  - An Heroku account
	- [Zeus](https://github.com/alayek/zeus)

## Test
```bash
# Create the box
zeus -l php -d <path> -o cake3

# test the box, going to http://localhost:8080 or http://192.168.56.101.

# Log on the box:
vagrant ssh

# Navigate to the site sources
cd /vagrant/www

# Initialise a git repo and commit
git init
git add .
git commit -m 'first commit'

# Login to heroku
heroku login

# Create a heroku app:
heroku create

# Push the site:
git push heroku master
# Optionnal: enable postgreSQL on Heroku:
heroku addons:create heroku-postgresql:hobby-dev

# Test the heroku box :
heroku open
```

## Notes
For now, cache is disabled on Heroku. You can help me with this issue (#2)