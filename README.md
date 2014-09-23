# bingo-tdp
=====

Update: I mentioned previously that I used a boilerplate to get the app started. I decided that it will probably just create confusion and it would be good practice to start from scratch. Although I used a specific file structure (see below), you'll probably understand why once you get through some of the tutorials.

## How to get started
First, clone this repository:

```
# Navigate to where you want to clone to
git clone https://github.com/steakholdrs/bingo-tdp
```

To run your app:

```sh
# Assuming meteor is already installed
cd /<path-you-cloned-to>/bingo-tdp
meteor
```

### What should you code?
Look under the [issues](https://github.com/steakholdrs/bingo-tdp/issues) page to see what needs to be implemented or fixed.

## Committing quick guide
After making changes to your local copy of the code, do

```
cd /<path-you-cloned-to>/bingo-tdp
git status
```

That will show you which files you changed. You can specify which files you want to add for a commit or you can just put in "." to add everything:

```
git add .
git commit -m 'add comment here of what you are pushing'
git push origin master
```

It will probably ask you to login.


### Packages included

* iron:router

You can also do the following command to get the most recent list of packages added:
```
meteor list
```


### Folder structure

```
lib/                    # <- any common code for client/server. 
lib/environment.js      # <- general configuration
lib/methods.js          # <- Meteor.method definitions
lib/external            # <- common code from someone else
## Note that js files in lib folders are loaded before other js files.

collections/                 # <- definitions of collections and methods on them (could be models/)

client/lib              # <- client specific libraries (also loaded first)
client/lib/environment.js   # <- configuration of any client side packages
client/lib/helpers      # <- any helpers (handlebars or otherwise) that are used often in view files

client/main.js   # <- subscriptions, basic Meteor.startup code.
client/index.html       # <- toplevel html
client/index.js         # <- and its JS
client/views/<page>.html  # <- the templates specific to a single page
client/views/<page>.js    # <- and the JS to hook it up
client/views/<type>/    # <- if you find you have a lot of views of the same object type

server/publications.js  # <- Meteor.publish definitions
server/lib/environment.js   # <- configuration of server side packages
```