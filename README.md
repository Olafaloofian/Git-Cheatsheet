### Git - The struggle, and the triumph.

Why the heck is git so confusing?!?

Git is a skill just like any other thing you've learned so far in your coding career. In fact, learning a version control software like git is one of the most essential items in your developer's toolbox. It's a huge headache at first, but just know that it'll make more sense and come much easier with some practice.

It is highly likely you will be asked questions about git during a coding interview, so it pays off to immerse yourself in this technology.

Let's go over a few git commands you should be using a lot! Each command will be followed by a short description, and if there are arguments to enter they will be represented as `<argument>`.

---

```
git add .
git commit -m 'Commit message here'
```

* You may already know what these do. You can stage and commit your code changes to your local machine using these commands.

---

```
git push
```

* This pushes your latest commit of the branch you are currently on to Github (or other online repository). Pushing means you believe to have the latest version of the code. If you don't have the latest version of the code, git will tell you to `git pull`. After pulling and resolving any issues, you should be able to push just fine.

* In the chance that your current branch doesn't already exist in the remote repository on Github, git will tell you that you should set an upstream origin. Use the command it provides to do so.

---

```
git pull
```

* Pulling means you are requesting the latest code from the remote repository on Github. If no one else has pushed since you last pulled, git will tell you that you are `Already up to date.`

* Pulling often results in merge conflicts. Make sure to carefully resolve the conflicts and consult with your team if necessary.

---

```
git merge <target branch>
```

* Working from the branch that you wish to merge another branch's changes to, run this command with the `target branch`'s name. For example, if you have a `development` branch that you wish to merge changes from `experimental` to, make sure you checkout to `development` and then run `git merge experimental`.

* `git merge` can result in merge conflicts just like pulling. Keep an eye out for conflict heads! `>>>>>>>>> HEAD`

---

```
git merge --abort
```

* Aborting a merge is possible and worth doing if you find out you've made some serious mistakes when attempting to resolve conflicts.

---

```
git checkout <target branch>
```

* This is how you switch to another branch. You can switch to any branch by using its name, or revert to previous changes by pasting the first bit of a commit code in.

---

```
git checkout -b <new branch name>
```

* This will create a new branch with the name you specify

---

```
git branch
```

* Will show all local branches, with your current working branch highlighted in some way

---

```
git branch -a
```

* Lists all branches, including remote Github branches, which will be designated as 'remote'. Helpful for checking out to a team member's remote branch to see their changes before they push.

---

```
git switch <remote branch>
```

* If you see a remote branch that you want on your machine, this command will allow you to create a local version of that branch.

---

```
git log
```
* Will display a list of commits in the current branch. If you are using VS Code, click the ^ terminal button to make this easier to read! Make note of the commit codes - you can use these to checkout to previous changes that you've committed in case you broke your code or are just unhappy with the current state of things.

---

```
git status
```

* Shows the status of the changes you have made to the current branch. This is useful for figuring out what you need to add and commit.

---

```
git remote -v
```

* If you are ever confused about where the remote code for your project is located, use this command to list them out (it's possible to have more than one remote).

---

```
git remote update
```

* This command refreshes information (such as branches) from the remote repositories. Use it if you don't see a remote branch on your local machine.

---

```
git blame
```

* A tool for figuring out who made certain changes to the code. Please use responsibly 😉

---

One more quick note - if you make some error (for example, trying to push when there is a more recent version already on Github), git does an amazing job of prompting you with what you need to do. Nine times out of ten git will give you a command to run, and you should run it. If you are super uncertain about the command, look it up and see what it does, then come ask us for help if you are still confused.
