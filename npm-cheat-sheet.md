# NPM Cheat Sheet for Beginners

## Installation

To install Node.js and npm, download from [nodejs.org](https://nodejs.org/).

## Initializing Projects

To create a new project:
```bash
mkdir myproject
cd myproject
npm init
```

## package.json Basics

- **name:** The name of your project.
- **version:** The version of your project.
- **scripts:** Scripts to run your commands.

## Installing/Uninstalling Packages

- To install a package:
```bash
npm install package-name
```
- To uninstall a package:
```bash
npm uninstall package-name
```

### Dependencies vs devDependencies

- **dependencies:** Required for your app to run.
- **devDependencies:** Only needed for development.

## Semantic Versioning

- **MAJOR.MINOR.PATCH**
- Example: `1.2.3` where `1` is MAJOR, `2` is MINOR, and `3` is PATCH.

## NPM Scripts

Define scripts in `package.json`:
```json
"scripts": {
  "start": "node index.js"
}
```

## Running Scripts

To run a script:
```bash
npm run start
```

## Updating Packages

To update all packages:
```bash
npm update
```

## npx Usage

Use `npx` to run packages without installing them globally:
```bash
npx package-name
```

## Publishing Basics

1. Create an account on [npmjs.com](https://www.npmjs.com/).
2. To publish your package:
```bash
npm publish
```
```
## Troubleshooting Common Errors

- **EACCES:** Permission denied. Fix it by changing directory permissions.
- **404 Error:** Package not found. Check if the package is published.

## Useful Commands

- `npm list`: View installed packages.
- `npm init`: Create a package.json file.
- `npm install`: Install project dependencies.
- `npm uninstall`: Remove an installed package.
