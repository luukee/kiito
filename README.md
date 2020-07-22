# kiito-theme-repo

KiiTO Spotify themes versions repo.
Plant Powered Superfuel https://drinkkiito.com/

1) Clone this repo
2) If KiiTO dev, duplicate current theme on Shopify: https://drinkkiito.myshopify.com/admin/themes / actions / download theme file
3) add it to your local repo (ex. ```kiito-themes/themes/[theme files]```)
4) Setup your GitHub repo: ```git init ``` at ```/themes/```
5) ![motifmate](https://i.ibb.co/HngWHhs/connect-motifmate-to-local-repo.png)

# Dev Process

1) In shopify duplicate the live theme
2) Rename the duplicated theme ex. orig theme: KiiTO 1.70, dup theme: KiiTO 1.71
3) Open Motifmate, select store and select duplicate theme.
4) In Motifmate select three dots ... `/ Folder / Connect`
5) Select the local theme repo ex. KiiTO (folder contains "`assets, config, layout, locales, sections, snippets, templates`")
6) In Motifmate click download button on far left.
7) Find the local repo ex. KiiTO and download.
    - This will allow you to have the exact files on the live theme, make changes and continue version control.
8) In terminal run `git status` to ensure you are on the correct repo.
9) Create the branch locally and then push to GitHub. A feature branch should always be 'publicly' available. That is, development should never exist in just one developer's local branch.

```
$ git checkout -b dup-theme-name master                 // creates a local branch for the new feature
```

```
$ git push origin dup-theme-name                        // makes the new feature remotely available
```

Periodically, changes made to master (if any) should be merged back into your feature branch.

```
$ git merge master                                      // merges changes from master into feature branch
```

When development on the feature is complete, merge changes into master and then make sure the remote branch is deleted.

```
$ git checkout master                                  // change to the master branch
``` 

```
$ git merge dup-theme-name                            // makes sure to create a commit object during merge
```

```
$ git push origin master                              // push merge changes
```

```
$ git push origin :dup-theme-name                     // deletes the remote branch
```