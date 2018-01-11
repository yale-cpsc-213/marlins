# Madlibs Activity
For this activity, you will use what you've learned about git to work collaboratively as a classroom to fill out a couple Madlibs. The class should be divided into groups responsible for Madlibs stories, nouns, verbs, adjectives, and adverbs.

## How To Setup This Activity

1. Form a group with your neighbors.
2. Make a Github account if you haven't already got one.
3. Fork the starter repository on Github.
  Forking means to make a copy of the code but attach it to your own Github repository so that you can make changes.

  Technically you are "cloning" the starter repo. GitHub calls this "forking" because they add some other
  bells and whistles on top. If you need more information, check out [https://help.github.com/articles/fork-a-repo/](https://help.github.com/articles/fork-a-repo/)

4. Login to [cloud9](https://c9.io/).  Or, if you want to work on your own computer, fine. In that case,
  you'll need to install node.js.

  You can create a cloud9 account by linking to GitHub.  Then, create a custom workspace, cloning from your forked repo.

  If working locally, you'll need to clone
  the starter repo using the `git clone`
  command. The clone url is displayed on GitHub, above the repository file browser.

5. Your group will be assigned to one of five responsibilities:
  stories, verbs, nouns, adjectives, or adverbs.

  Checkout a new branch with a good name. Mine is going to be "kyle-verbs". Yours should
  be something different. This will be a command like
  ```
  git checkout -b kyle-verbs
  ```


6. Take a look around at the files

  Familiarize yourself where everything lives. You'll use the shell commands `cd` to change
  directories and `ls` to see what is each directory.

7. Create a new branch

  It might help to give your group a name. Then, you can make your branch something like
  "fantastic-falcons-verbs" or "bouncing-bears-adverbs".

7. Create a new file

  Technically, you can also edit existing files, but that will make my job of merging harder!
  If you want to make a new file of verbs, you should first choose a file name. For example,
  if I chose "kyles-fun-verbs" I might make a file at
  `madlibs/pos/verbs/kyles-fun-verbs.js` and it might look like this:

  ```javascript
  module.exports.verbs = [
    'sleep',
    'spit',
    'spin'
  ];
  ```

  You can use the command `nano` to create and edit files.  You may also use the cloud9 editor, or a local text editor you have installed, like [atom](https://atom.io/).

  For example `nano pos/verbs/my-new-file.js` will create the file `my-new-file.js` in the directory `pos/verbs`.

8. Check your code works.

  Assuming you have [node installed](https://nodejs.org/en/), run the following:

  ```
  npm install
  ./node_modules/.bin/gulp
  ```

  The app is now accessible in your browser.  Ensure
  your changes didn't introduce any errors. If you screwed up your js, your app will
  likely crash and you just fix it.

9. Commit your changes and share them

  First, take a look at the status of your work

  ```
  git status
  ```

  It should show what files are new and what files are changed. Now, you want
  to add the new files, try the `git add` command. You'll need to supply a file name.

  Once you've added your changes to the "staging area", you want to make a commit. This
  is a command like

  ```
  git commit -m "Added some verbs for class"
  ```

  Now, push your changes up to GitHub.

  ```
  git push origin BRANCHNAME
  ```

  where `BRANCHNAME` is the name of your branch.

10. Go to GitHub, find your fork and the new branch, then make a pull request

  Pull requests let you tell others about changes you've pushed to a repository on GitHub. Once a pull request is sent, interested parties can review the set of changes, discuss potential modifications, and even push follow-up commits if necessary.

  Click on the logo at right to get started.
  ![Starting the pull request](https://github.com/yale-cpsc-213/madlibs/blob/master/images/pull.png)

  Then, once you get to another page, click the blue link.
  ![Continuing the pull request](https://github.com/yale-cpsc-213/madlibs/blob/master/images/pull2.png)

  Finally, click the create button to checkout the commit.
  ![Finishing the pull request](https://github.com/yale-cpsc-213/madlibs/blob/master/images/pull3.png)

  If you need extra help, check this out [https://help.github.com/articles/using-pull-requests/](https://help.github.com/articles/using-pull-requests/) or just come see a TA.

11. The instructor will merge in everybody's work. Bother Kyle or the TAs if nothing's working.

## Some hopefully helpful notes

* Each Story group should create a new html file to make a story. Stories should be put into the stories folder `/stories`. An example of a story is already in the folder (see `/stories/layout.html` or `/stories/layout2.html`) **Don't change these example files!** Make new ones!

  Stories are written in HTML! We are not going to be styling it, so forget about the CSS. Remember the general structure of HTML code: (No need to include the DOCTYPE stuff here).

    ```html
    <html>
      <body>
        Insert Code Here.
      </body>
    </html>
    ```
  You may notice that there are weird `{{...}}` everywhere in the example HTML codes. This stuff is super important! It tells our little node app that we need a(n) adjective/verb/adverb/noun at a certain place. When you write your own stories, make sure to do the same! For example, to denote an adjective, used `{{adjectives.get()}}`. The others follow the same style!

* The adjective, noun, and verb groups should work on their files. Adjective, noun, and verb files should be put in their respective folders. For example, verbs should be put in `/pos/verbs/verbs.js`.

  Examples of verbs, adjectives, etc files are found in the corresponding `starter.js` file in the folder in `/pos`. **Don't change these example files!.** Instead, make a new file.

    ```javascript
    module.exports.adjectives = [
      Insert Words Here.
    ];
    ```
  Notice that there is a very specific structure when listing the words in this file. Our node app waits to grab the array of words that is exported from this file. Therefore, don't forget the `module.exports.adjectives = ...`!

## Have Fun and Ask Questions!

Something to keep in mind as you are working: Make sure you comment your code. You may not need it but it's generally a good idea so that you and others can understand what is going on.
