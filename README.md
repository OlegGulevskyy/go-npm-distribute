# Write Go code, distribute through NPM like JS

NPM provides simplicity for distribution. Lack of security for NPM packages allows you to execute any binary, as long as it's distributed through NPM.
If a binary compiled and distributed in any other ways (like archiving it, sharing it with a friend etc) -- it has to be signed, otherwise OS security will not allow you to use it, even in terminal.

I put together a barebone project that allows to create CLI (using Cobra-CLI) and distribute it via NPM.
Simply copy the repo, remove current git from its directory and initialise a new git (`git init`).

## How to use it

General flow is:

1. Do the changes you need to (write logic, update files, whatever)
2. Commit the changes
3. Use `task patch / minor / major` depending on which version you need to bump (look up semver for more info)
4. Use `task release`, this will build the binaries, archive them and upload to GitHub repository as package
5. Use `task publish-npm`, which will then take all the uploaded archives to GitHub previously and publish them to your NPM account

Now you can do `npm install {your package name}`

More detailed instructions to come
