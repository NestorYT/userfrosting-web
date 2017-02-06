# UserFrosting main site

https://www.userfrosting.com

This is the repository for the main UserFrosting 4 website.  It is built with the flat-file CMS [Grav](http://getgrav.org).

## Local installation

### Step 1 - Install Grav

This application uses the [Grav](https://learn.getgrav.org/) CMS.  This repository does not contain a full Grav installation - rather, it just contains the contents of Grav's `user` directory, which is where all of our custom content, themes, and assets live.  This was done as per the [recommendation on Grav's blog](https://getgrav.org/blog/developing-with-github-part-2), to make it easier to deploy changes to the live server.

To install this website on your computer, first [install grav core](https://getgrav.org/downloads) in a project folder called `userfrosting-web` under your webserver's document root folder. Then, find the `user` folder inside of your project folder.  Delete the contents of the `user` folder and clone this repository directly into the user folder.

When you're done it should look like this:

```
htdocs/
└── userfrosting-web/
   ├── assets/
   ├── ...
   ├── user/
       ├── .git
       ├── accounts/
       ├── assets/
       ├── config/
       └── ...
   └── ...

```

### Step 2

Grav needs your webserver to be able to write to certain directories.  In OSX with XAMPP installed, this won't work by default.  To deal with this:

Add default webserver user `daemon` to OSX's `staff` group (which already has the necessary permissions for writing to files/directories):

`sudo dseditgroup -o edit -a daemon -t user staff`

## Credits

Favicons were generated with https://realfavicongenerator.net/
