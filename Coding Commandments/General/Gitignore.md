Use `.gitignore` file effectively. It should contain non-source resources, including but not limited to:
*  Editor specific files e.g. `.vscode`, `.idea/` etc
*  Dependencies e.g. `node_modules` or any other binaries which can be resolved as an external dependency through `package.json/pom.xml/requirements.txt`
*  Environment files e.g. `.env.development.local` etc
*  Compiled code e.g. contents of your `build` or `dist` directories
*  Log files