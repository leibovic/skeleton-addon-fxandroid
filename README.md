# Skeleton for an Add-on in Firefox on Android

This code supplies the basic bits and pieces needed to build a simple,
restartless add-on for Firefox on Android, which uses a native widget UI.
Since Firefox on Android does not use XUL for the UI, building an add-on is a
little different than building an add-on for desktop Firefox.

For more information about building mobile add-ons, please see:
https://developer.mozilla.org/en-US/Add-ons/Firefox_for_Android

## Using the Skeleton

Step 1: Edit the `install.rdf`
  * Please change the ALL CAPS areas with text specific to your add-on.

Step 2: Add code to `bootstrap.js`
  * The current code adds some menus, doorhangers and context menus that don't do very much right now.

Step 3: Edit `build`
  * Update this file to specify a file name for your XPI, as well which version of Firefox you want to use to test the XPI file.

Step 4: Run `./build`
  * This creates the XPI and optionally pushes it to your device. You must have [adb](http://developer.android.com/tools/help/adb.html) installed for the push step to work.

## Using volo

You can use [volo](http://volojs.org/) to quickly bootstrap your add-on from this template.

volo requires [node](http://nodejs.org/) to run. To install volo:

    npm install -g volo

After installing volo, to create a new directory for your add-on, run:

    volo create youraddon https://github.com/leibovic/skeleton-addon-fxandroid/archive/master.zip

This will create a new directory `youraddon`, which holds all the files for your add-on.

