# scaffolds

Scaffolds for various tooling and configuration. Organised by branch.

##### Branches (Scaffolds)

- gulp-pattern
    - [go to branch](https://github.com/johnnycopperstone/scaffolds/tree/gulp-pattern)
    - [readme](#gulp-pattern)

##### Using Scaffolds

Using scaffolds as a helpful development tool is very easy. All you need to do is add this repository's url as a remote in your repo. I generally prefer to give the remote a name like `scaffolds` or `tooling` to indicate what it's for.

    git remote add scaffolds https://github.com/johnnycopperstone/scaffolds.git

That's pretty much it. Whenever you want to use one the scaffolds in your project, for example setting you gulpfile according to [gulp-pattern](https://github.com/snslss/gulp-pattern) conventions, simply fetch this repo and then merge the desired scaffold (branch) into your branch.

    git fetch scaffolds
    git merge scaffolds/gulp-pattern

Ideally, you wouldn't have the same files / folders in your repo yet, so you shouldn't have any merge conflicts.

##### Developing Scaffolds

Each branch ignores specific files you wouldn't want merged in when merging into your repo, however are needed for dev of the scaffold. To avoid conflicts in `.gitignore`, and adding files to your `.gitignore` you may not want, these are added locally in `.git/info/exclude`. This won't interfere with your repo. Each branch's README section (found here) should list the files to ignore, so you can add these to your exclude if you were to work on one.

# list of scaffolds

### gulp-pattern

This scaffold sets up your init `gulpfile.js`, with a ready implementation
of [gulp-pattern](https://github.com/snslss/gulp-pattern). It also creates the folder structure for your gulp tasks and workflows.

##### Required modules

These are the required node modules you need with this scaffold. Don't forget to add them to your `devDependencies`.

    gulp
    lodash

##### Ignored files

    node_modules/
    package.json
