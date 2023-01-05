# TypeScript Template Creator

Create a new TypeScript project in one easy step! No more installing packages and setting up boilerplate just to write some code!

## Steps to use:

1. Clone this repository with `$ git clone --depth 1 https://github.com/aarondill/ts-template <name-for-your-folder>`
2. Navigate to the folder you just cloned: `$ cd <name-for-your-folder>`
3. Run the init script: `$ ./init`

Optionally, use `./init -y` or `./init --yes` to answer yes to all prompts. This will **NOT** create a github repository.
This is the only currently supported option. Other arguments will have no effect.

### OR use this _one_ command!

```bash
read -rep 'What to call your folder? ' folderName && [[ -n "$folderName" ]] && git clone --depth 1 https://github.com/aarondill/ts-template "$folderName" && cd "$folderName" && ./init
```

Simply answer the quick questions, let it install DevDependencies and enjoy!

## Features included:

- Automatically create local git repo
- Optionally create Github repository (**Requires `gh` CLI**)
- Support for Jest, with built-in config
- Config file for eslint with TypeScript (optional root property)
- .gitignore with many popular files already listed. **Please Check Contents Before Committing!**
- .vscodeignore for easy configuration if creating vscode extensions. Feel free to remove in other cases.
- MIT License already included
- Tsconfig with strict mode activated
- Tsc outputs to ./dist from ./src
- Package.json with lint, build, test(optional), and watch scripts already created
- File system setup with tests, src, and resources folders, along with index.ts and index.test.ts files
- Release-it included to allow easy releasing, with config file included. Run `npm run release` in your new project to create a release.
- No (regular) dependencies will be added to your project

## Notes:

- Project name is validated against the [NPM project name requirements](https://docs.npmjs.com/cli/v9/configuring-npm/package-json#name). Uppercase letters are automatically converted to lowercase and spaces are converted to dashes. Other requirements must be manually achieved.

- To allow Release-it to automatically create Github Releases, instead of _just_ tags, set the environment variable `RELEASE_IT_GITHUB_TOKEN` to a Github Token with proper authentication. [See more here](<https://github.com/release-it/release-it/blob/master/docs/github-releases.md#automated:~:text=Obtain%20a%20personal%20access%20token%20(release%2Dit%20only%20needs%20%22repo%22%20access%3B%20no%20%22admin%22%20or%20other%20scopes).>). Without this token, Release-it will fallback to a web browser with defaults filled in.
