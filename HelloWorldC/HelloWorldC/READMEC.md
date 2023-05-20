If VSCode is used then make tasks.json contain gcc build tools and make sure mingw is in path

Here is the content of the tasks.json:

``` {
    "version": "2.0.0",
    "tasks": [
        {
            "label": "compile and run C",
            "type": "shell",
            "command": "gcc '${file}' -o ${fileBasenameNoExtension} ; ./${fileBasenameNoExtension} ",
            "presentation": {
                "reveal": "always",
                "panel": "shared"
            },
            "group": {
                "kind": "build",
                "isDefault": false
            }
        }
    ]
}
```
