## Workflow for writing chapters

We are orientating ourselves to the feature branch workflow as explained here: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

In summary: For each chapter that is edited, the author(s) create a new branch. E.g. if chapter 03-00-xx.Rmd is edited, than the author creates a new branch `writing-of-03-00`. How to create a new branch depends on the software you are using. If you use the terminal see [here](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches). __Please make sure that all of your work is done in the corresponding branch!__ Don't hesitate to contact us if you encounter something strange or think you have made changes in the wrong place. It's no big deal to revert changes and repair it if they aren't too much.

Note that you have to set the user name and email to be able to push to a repository:
```
git config --global user.name "my_user_name"
git config --global user.email "my_user_email"
```

The workflow (explained for the terminal) is:

1. Clone the repository: `git clone https://github.com/compstat-lmu/seminar_nlp_ss20.git` (you can also use SSH if enabled)
1. Make sure you are in the directory of the repo
1. Create a new branch: `git checkout -b writing-of-xx-xx`
1. Push the branch on github: `git push origin writing-of-xx-xx`

Then just work in your branch. Make also sure to pull the latest changes before working again on your chapter:

1. Make sure you are in the directory of the repo
1. Pull latest changes `git pull origin writing-of-xx-xx`

Pushing changes made in the chapter are done by commits where you give a short description about the changes:

1. Add the files you want to push online: `git add 03-00-xx.Rmd` (to add all files at once use `git add --all`)
1. Write a short description what you have done: `git commit -m "add first subchapter about something"`
1. Push the branch on github: `git push origin writing-of-xx-xx`

It's good practice to not push too many changes at once. It's better to have smaller commits. Also don't forget to push after you are done working! In the case of any crash of your system (or RStudio) it may happen that your work is gone if you haven't pushed your local changes.

Another note: You can use `git status` to see what files contains local changes.

## Naming scheme for the repo

### Structuring of files

There are four subdirectories:

- code
- data
- figures
- results


### Naming convention

Code, data, figures, and results are stored in subdirectories in the directories mentioned above named as the chapter itself. E.g. the R code `fit--model.R` for the chapter `03-00-xx.Rmd` is saved in `code/03-00-xx/fit-model.R`. The same holds for data, figures, and results. I personally like it to have an additional order in the naming of my figures etc. corresponding to the order in the chapter, e.g. `01-bla.png`. Have a look at the `000-test.Rmd` to get an idea how the repo should be structured.

__Another note about figures:__ Please save your figures as png or jpg since it is not possible to show pdf images in the html booklet.
