# Build Task for VSCode:

# Run .ts-files with node.js

---

## What is this?

The tasks.json-file defines a build task for the famous text-editor Visual Studio Code. It's goal is to transcript the TypeScript-file (.ts) you are currently editing to a JavaScript-file (.js) and to run that outcoming js-file with node.js in your default shell (the shell you defined as default in Visual Studio Code)

---

## Dependencies

To run this build task you have to install on your system this applications:

- node.js

- npm

Then open your favorite shell and use this command to install the TypeScript-transcriptor:

```shell
npm install -g typescript 
```

If that command doesn't work on your favorite Linux-distro, you may have to run it with sudo.

---

## Usage

To run the build task you have to take a few simple steps first:

1. Download the tasks.json-file or clone the whole repository.

2. Move the tasks.json-file into the .vscode-directory of your VSCode-workspace.

3. Open your VSCode and create a new TypeScript-file (new file with file-extension .ts) and type there some random TypeScript-code. You can use this snippet, for example:
   
   ```typescript
   var msg:string = "Hello World!"
   console.log(msg)
   ```
   
   We only need that file to configure and test the build task, so the code doesn't have to be very complex.

4. Then open in your VSCode the tab "Terminal" and goto "Configure Default Build Task...". There you have to choose the option "node_runner_task(ts)".

5. At the end you have to run the configured Build Task. To do so, open "Terminal" > "Run Build Task" or just hit `STRG` + `SHIFT` + `B`

6. The build task opens now two new shells. In the first one there is working the transcriptor. The second one runs the succesfully transcipted js-file with node.js. It's outcome is "Hello World!". Congratulations!
