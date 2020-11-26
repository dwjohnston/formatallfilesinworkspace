This a fork of the formatall extension that I've used to update all imports in the workspace. 

I couldn't work out how to configure it to instead of `editor.action.format` to `source.addMissingImports` , so instead I set it to: `editor.action.insertLineAfter`, and have an 'on save action ' to `source.addMissingImports`. /shrug

This extension isn't published, I just used the dev mode to do this as a one time task. 

## The whole process: 

The purpose of this was to change all imports of '../..' to '../../MoreDirectRefernce/ToToTheComponent'. 

1. Delete all '../..' imports using the find replace function of VSCode and a regex. 
2. Open the modified plugin in a fresh VSCode window. Press F5
3. In the new window that is created, add the source folder that you want to update imports of. 
4. Add this to your settings.json: 
```
"editor.codeActionsOnSave": [
    "source.addMissingImports"
]
```
5. Possibly important! You might want to delete your node_modules folder. This is to, in my case, prevent VScode from importing from @material-ui, when it does the auto imports, where I want to import from my src folder. 
6. Run the plugin via the command pallete. 
7. This will open and modify every file in your project. 
8. Close all the files, the imports will be auto added. 

