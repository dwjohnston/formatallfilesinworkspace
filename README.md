This a fork of the formatall extension that I've used to update all imports in the directly. 

I couldn't work out how to configure it to instead of 'editor.action.format' to 'source.addMissingImports' , so instead I set it to: 'editor.action.insertLineAfter', and have an 'on save action ' to 'sourceAddMissingImport's. /shrug

This extension isn't publish, I just used the dev mode to do this as a one time task. 

## The whole process: 

The purpose of this was to change all imports of '../..' to '../../MoreDirectRefernce/ToToTheComponent'. 

