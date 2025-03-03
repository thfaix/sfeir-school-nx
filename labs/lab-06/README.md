# Lab 06: _`nx affected`_ command

We will be working on this workspace:

![Alt text](../lab-common/lab-nx-multi-stacks-monorepo.png)

## Lab Setup

1. Clone the repo with: `git clone https://github.com/tinesoft/nx-multi-stacks-monorepo.git`
2. Open the folder in VSCode or IDE of choice
3. Run `npm ci` to install  necessary **NPM** dependencies

## Running a **single target** on all projects affected

### Running `build` target on all projects affected

1. Open a Terminal
2. Run "`npx nx affected -t build`"
3. Run again "`npx nx affected -t build`" executor to see **computation caching** in action
4. Run "`npx nx affected -t build --skip-nx-cache`" 
    * what do you notice?
5. Run "`npx nx affected -t build --parallel 4`" executor to see **parallelization** in action
    * Increase/Decrease the value of `--parallel` option to see how it affects the command

### Running `build` target on specific projects affected

1. Open a Terminal
2. Run "`npx nx affected -t build --projects=ng* --skip-nx-cache`"
3. Run "`npx nx affected -t build --exclude=react* --skip-nx-cache`"
4. Run "`npx nx affected -t build --projects=boot* --skip-nx-cache`"

## Running **multiple targets** on all projects affected

### Running `build`, `test` tasks on all projects affected

1. Open a Terminal
2. Run "`npx nx affected -t build,test`"
3. Run again "`npx nx affected -t build,test`" executor to see **computation caching** in action
4. Run "`npx nx affected -t build,test --skip-nx-cache`" 
    * what do you notice?
5. Run "`npx nx affected -t build,test --parallel 4`" executor to see **parallelization** in action
    * Increase/Decrease the value of `--parallel` option to see how it affects the command

### Running `build`, `test` task on specific projects affected

1. Open a Terminal
2. Run "`npx nx affected -t build,test --projects=ng* --skip-nx-cache`"
3. Run "`npx nx affected -t build,test --exclude=react* --skip-nx-cache`"
4. Run "`npx nx affected -t build,test --projects=boot* --skip-nx-cache`"
