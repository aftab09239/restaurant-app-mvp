# Fixes and Run Instructions

## Changes made

- Pinned Expo, React, React Native, and web runtime dependencies instead of using `latest`. This prevents npm from selecting mutually incompatible major versions.
- Added the web dependencies needed by `expo start --web`.
- Kept the existing app features and source code intact.

## Clean installation (Windows PowerShell)

Run these commands from the `restaurant-app-mvp` folder:

```powershell
# If node_modules exists and you want a clean install, remove it with PowerShell syntax
Remove-Item -Recurse -Force node_modules -ErrorAction SilentlyContinue
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm.cmd install
npx.cmd expo install --check
npx.cmd expo start --web
```

If Expo reports that a dependency is not compatible, run `npx.cmd expo install --fix` and then restart Expo with `npx.cmd expo start --web -c`.

## Important

This ZIP is the version that was uploaded for review. It does not contain every file visible in your VS Code screenshot, so it may not be identical to the project currently on your computer. Back up your current folder before replacing anything.
