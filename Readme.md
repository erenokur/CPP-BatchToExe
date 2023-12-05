## CPP-BAT-TO-EXE

Simple C++ program to run batch files with exe files. This is very easy way to make exe files.

### How to use it

open cpp file changed bat name as your bat file name and compile it with g++ compiler.

### How to compile it

To execute on command line:
g++.exe -fdiagnostics-color=always -g BatConvertExe.cpp -o BatConvertExe.exe

### To use it with VSCode:

create a task.json file in .vscode folder and add this code to it:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "type": "cppbuild",
      "label": "C/C++: g++.exe build active file",
      "command": "g++.exe",
      "args": [
        "-fdiagnostics-color=always",
        "-g",
        "${file}",
        "-o",
        "${fileDirname}\\${fileBasenameNoExtension}.exe"
      ],
      "options": {
        "cwd": "${fileDirname}"
      },
      "problemMatcher": ["$gcc"],
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "detail": "Task generated for creating exe."
    }
  ],
  "version": "2.0.0"
}
```

create a setting.json file in .vscode folder and add this code in it:

```json
{
  "files.associations": {
    "iostream": "cpp"
  }
}
```

All settings are made just press : CRTL + Shift + B
