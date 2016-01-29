# Node-Git-Hooks
Examples of Git hooks written in node with script to initialise them. Examples have been tested on OSX, Linux and Windows.

Simply run `npm run git:init`.

## Customisable hooks

There are [many](https://git-scm.com/docs/githooks).

## Examples
 + pre-commit: Add a test script to the package.json to see a pre-commit hook running tests before commit.
 + pre-push:   Try pushing to master to see you fail!

## Why Initialise?

 + `git/init.js` is needed to copy over hooks found in `git/hooks` into `.git/hooks` folder.
 + Uses node modules `fs` and `path` to do so.
 + This is required as the .git/ file being local and can't be shared over git.
 + `chmod +x` is used on each script to allow it to be executable more than one time!

You could just copy and paste but that would be boring and a one liner means your team of developers will be slightly less reluctant to add hooks to their flow!

### Suggestions
I have no idea whether what I've done is best practice so please create issues with comments, suggestions and questions.

#### TODO

 + Check to see if any hooks are in place and use renameFileSync to create hook.old files to be used again.
