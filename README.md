# TypeScript Template Creator

Create a new TypeScript project in one easy step! No more installing packages and setting up boilerplate just to write some code!

## Steps to use:

1. Clone this repository with `$ git clone https://github.com/aarondill/ts-template <name-for-your-folder>`
2. Navigate to the folder you just cloned: `$ cd <name-for-your-folder>`
3. Run the init script: `$ ./init`

Optionally, use `./init -y` or `./init --yes` to answer yes to all prompts. This will **NOT** create a github repository.
This is the only currently supported option. Other arguments will have no effect.

### OR use this _one_ command!

```bash
read -rep 'What to call your folder? ' folderName && [[ -n "$folderName" ]] && git clone https://github.com/aarondill/ts-template "$folderName" && cd "$folderName" && ./init
```

Simply answer the quick questions, let it install DevDependencies and enjoy!

## Features included:

- Automatically create local git repo
- Optionally create Github repository (**Requires `gh` CLI**)
- Support for Jest, with built-in config
- Optional config file for eslint
- .gitignore with many popular files already listed. **Please Check Contents Before Committing!**
- .vscodeignore for easy configuration if creating vscode extensions. Feel free to remove in other cases.
- MIT License already included
- Tsconfig with strict mode activated
- Tsc outputs to ./dist from ./src
- Package.json with lint, build, test(optional), and watch scripts already created
- File system setup with tests, src, and resources folders, along with index.ts and index.test.ts files

## Notes:

Project name is validated against the [NPM project name requirements](https://docs.npmjs.com/cli/v9/configuring-npm/package-json#name). Uppercase letters are automatically converted to lowercase and spaces are converted to dashes. Other requirements must be manually achieved.
