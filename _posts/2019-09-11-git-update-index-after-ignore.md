# How to make Git "forget" about a file that was tracked but is now in .gitignore?

## With a file:

Use bellow command:

```
git update-index --assume-unchanged "your-file-path"
```

## With a folder, do following [steps](https://stackoverflow.com/questions/12288212/git-update-index-assume-unchanged-on-directory):

Step 1:

cd into the folder you want to assume is unchanged

Step 2:
```
git ls-files -z | xargs -0 git update-index --assume-unchanged
```
