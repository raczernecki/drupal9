# Docksal powered Drupal 9

## Features

- Vanilla Drupal 9 with preinstalled admin toolbar and material design theme
- Editable init script `fin init` [example](.docksal/commands/init)
- Using the [default](.docksal/docksal.env#L9) Docksal LAMP stack with [image version pinning](.docksal/docksal.env#L13-L15)
- PHP and MySQL settings overrides [examples](.docksal/etc)
- Drush aliases [example](drush/aliases.drushrc.php) (`drush @docksal status`)

## Security notice

This repo is intended for quick start demos and includes a hardcoded value for `hash_salt` in `settings.php`.  
If you are basing your project code base on this repo, make sure you regenerate and update the `hash_salt` value.  
A new value can be generated with `drush ev '$hash = Drupal\Component\Utility\Crypt::randomBytesBase64(55); print $hash . "\n";'` 
