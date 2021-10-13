# Work in Progress

...

![content boxes](Documentation/Images/content-boxes.JPG)

![delete action](Documentation/Images/delete-action.JPG)

![more button](Documentation/Images/more-button.JPG)

![new boxes](Documentation/Images/new-buttons.JPG)

# How to

## In your composer-installed TYPO3 v11.5.x:

```shell
composer config extra.enable-patching true
composer require typo3-ux/page-module-pilot
```

## Or spin up a new ddev instance:

```shell
mkdir my-typo3-site
cd my-typo3-site
ddev config --project-type=typo3 --docroot=public --create-docroot
ddev start
ddev composer create "typo3/cms-base-distribution:^11"
ddev composer config extra.enable-patching true
ddev composer require typo3-ux/page-module-pilot

# todo: composer-patch does not get active here. Workaround:
rm -rf public/typo3/sysext/backend
ddev composer install
# /todo

ddev exec touch public/FIRST_INSTALL
ddev launch
```

