A PHP API for Destiny The Game
===========

[![Build Status](https://travis-ci.org/aFreshMelon/destiny-php.svg)](https://travis-ci.org/aFreshMelon/destiny-php)

This is an easy to use PHP API to access all sorts of information about any Destiny account. 
This includes characters equipment, progression and all sorts of other information.

**Please note that this project is still in BETA!**

Usage
-----

Install the latest version with `composer require afreshmelon/destiny dev-master`

```php
<?php

require 'vendor/autoload.php';

use Destiny\Client;

// Create a new instance of the client
$destiny = new Client;

// Find a player
$player = $destiny->fetchXboxPlayer('aFreshMelon');

// Get the first character
$firstCharacter = $player->characters->first();

// Output the characters level
echo $firstCharacter->characterLevel;