# scoop-strike3
Instructions for installing Strike3 on Windows using Scoop.

## Steps for each new Strike3 build
1. Compress the files and folders created by the Xojo build process into a `.zip` file and rename to `strike3-XXX-win64.zip` (where `XXX` is the version number). The version number must be bigger than the current one for Scoop to correctly update Strike3
2. Draft a new release for Strike3 and upload the Windows and macOS files. Strike3 is too big to be hosted by GitHub so it needs to be self-hosted. Copy the URL for the Windows download
3. Update the `version` key to the new version number
4. Set the URL in `strike3.json` to the Windows zip URL
5. Determine the Windows zip file's SHA256 value with the Terminal command: `openssl sha256 [file]`
6. Replace the SHA56 value in the JSON file `hash` key with the new one
7. Commit and push the changes in the JSON file to GitHub.