# Git & Github Resources

- [Git Command Explorer](https://gitexplorer.com/) - Find the right commands you need without digging through the web.

- [Learn Git Branching](https://learngitbranching.js.org/) - Visual and interactive way to learn Git

- [OhShitGit](https://ohshitgit.com/)

- [Ross's Git Guide](https://github.com/GregorRoss/ELGA/blob/main/git-guide.md) - Git guide for pushing changes and initiating pull requests on Github

- [Git Commands w/ examples](https://dzone.com/articles/top-20-git-commands-with-examples) - Top 20 Git Commands

- [Github Cheat Sheet by Tim Green](https://github.com/tiimgreen/github-cheat-sheet) - Collection of cool hidden and not so hidden features of Git and GitHub

- [Github Skills](https://github.com/skills) - Interactive courses for learning GitHub

---------------

### Github README:

- [Github Readme Examples](https://github.com/abhisheknaiidu/awesome-github-profile-readme#retro-)

- [Readme Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)

_____

### [Git Basics](https://gist.github.com/cblunt/860360)
##### Quick Summary

    cd my_project

    git init .
    git add . # add everything
    git commit -m 'Initial commit'

... make some changes ...

    git add .  # adds all changed files to the stage to be committed
    git commit -m 'Some changes'

    git push origin master

... make some more changes ...

    git add index.html css/screen.css # only add these two files to the stage
    git commit -m 'Changed index and screen'

##### View the commit history

    git log

##### Add a remote repository
    
    git remote add origin git://server/my_project.git 
    # git remote add origin file:///path/to/local/repositories/my_project.git # For a local (disk) repository

... and push your changes to it ...

    git push origin master

##### Restoring a file from the repository (replace your working copy)

1. Write some content to index.html

        echo "Hello" > index.html
        cat index.html
        #  => Hello

2. Commit the new index.html

        git add index.html
        git commit -m 'Hello index.html'

3. Overwrite the original content 
    
        echo "Oops" > index.html
        cat index.html
        # => "Oops"

4. Restore the original index.html from the repository
    
        git checkout index.html 
        $ cat index.html
        #   => Hello

## Long Version

Assuming the following project:

    mkdir -p my_project my_project/images my_project/css my_project/js
    echo "<p>Hello World</p>" > my_project/index.html
    touch my_project/js/application.js my_project/css/screen.css

    cd my_project

Create a repository, and commit initial files.

    git init .
    git add .
    git commit -m 'Initial commit'

Change and add files. 

    echo "<p>The world has changed.</p>" > index.html
    git add index.html

`index.html` is now staged. This is a middle-ground between the repository and your working copy. A staged file is not yet committed to the repository, but is independent of any further changes to your working copy.

What this means is that you can continue working on index.html, but still commit the previously staged version:

Commit staged files to the repository...

    git commit -m 'Changed content of index.html'

...or re-add your changed working copy

    echo "<p>It changed again</p>" > index.html 
    git add index.html
    git commit -m 'Changed content of index.html'

