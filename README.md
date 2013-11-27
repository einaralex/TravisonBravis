TravisonBravis
==============

Simple script for Travis-CI to push a succesful build onto a another branch

#HOW TO#

1. Install Travis `gem install travis`
2. Go to your [Travis-CI](https://travis-ci.org/profile) and enable your repository.
3. Go to your GitHub repository settings > Service Hooks > Travis and choose Update settings.
4. Go to your [GitHub](https://github.com/settings/applications) profile settings > Applications > Personal Access Tokens and choose Create new token.

    Copy and keep. Choose a descriptive name e.g. travis-yourrepo
    
5. Locate your local repository and encrypt your token  `travis encrypt GH_TOKEN="yourtokenhere" --add`
    
    It will then show up in your .travis.yml file.
    
```
env:
    global:
      - secure: yourtokenhere
```
Replace .travis.yml with your settings.



```
- GH_REPO="username/yourrepo"
- GH_NAME="username"
- GH_EMAIL="example@email.com"
- DEVELOPMENT="branch1"
- SUCCESSFUL="branch2" 
```
 

and you're good to go!


[![Build Status](https://travis-ci.org/einaralex/TravisonBravis.png?branch=master)](https://travis-ci.org/einaralex/TravisonBravis)
