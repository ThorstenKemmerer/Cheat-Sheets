# pnpm Cheat Sheet for Beginners

## Installation
To install pnpm globally, run:
```bash
npm install -g pnpm
```

## Init
To create a new project with pnpm, run:
```bash
pnpm init
```
This will guide you through creating a package.json file.

## Adding Packages
To add a package, use:
```bash
pnpm add <package-name>
```
For example, to add lodash:
```bash
pnpm add lodash
```

## Removing Packages
To remove a package, use:
```bash
pnpm remove <package-name>
```
For example, to remove lodash:
```bash
pnpm remove lodash
```

## Development Dependencies
To add a package as a dev dependency, use:
```bash
pnpm add <package-name> --save-dev
```

## Global Installs
To install a package globally, use:
```bash
pnpm add -g <package-name>
```

## Running Scripts
To run a script defined in package.json, use:
```bash
pnpm run <script-name>
```

## pnpm Store
pnpm uses a global store to save disk space and improve performance. You can access the store by running:
```bash
pnpm store status
```

## Workspaces Basics
To manage multiple packages in a monorepo, set up a `pnpm-workspace.yaml` file:
```yaml
packages:
  - 'packages/*'
```
Then, you can add or remove packages in any of the workspaces.

## Updating Packages
To update packages, use:
```bash
pnpm update
```

## Common Troubleshooting Tips
1. If you encounter issues with the store, try:
   ```bash
pnpm store prune
```
2. To force install packages, use:
   ```bash
pnpm install --force
```
3. Check for outdated packages with:
   ```bash
pnpm outdated
```

Happy Coding!