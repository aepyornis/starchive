# ★ Starchive ★

Store your starred github repos offline!

I like to star repos on github. But I'm also a little paranoid. What if github disappears? Or a repo I like is removed? I also often find myself looking up the source code of a project by going to it's page on github.com. It's usually nicer to just look at the code locally.


## How to use

It requires ruby, bundler, and one gem, github_api. If you already have bundler installed, the script will install the gem on it's first run.

The script can be configured using two environment variables: *GITHUB_USER* and *STARCHIVE_FOLDER*

I use this to make a copy of my own stars, but because stars are public, you can make an archive of any github user.

The default location of the archive is "~/starchive"

Examples: 

To make a copy of my stars:

``` sh
GITHUB_USER=aepyornis ./starachive
```

Using a different location:

``` sh
GITHUB_USER=aepyornis STARCHIVE_FOLDER=/mnt/usb/starchive ./starachive
```

To keep your archive up-to-date, you can re-run the script. It will clone your new stars and issue `git fetch --all` for your existing copies.

**Note**: if you star a lot of repos this will take up a lot of space!!
