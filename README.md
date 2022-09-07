# LUA Sandbox
Lua Sandbox using LRDB

## Build libraries
1. Change directory to `ext`.  
  ```
  $ cd ext
  ```

2. Run make.  
  ```
  $ make lib
  ```

## Build host
Build host using Visual Studio Code with CMake extension.

## Run host
Run host from terminal or within Visual Studio Code.
```
$ ./build/lua-sandbox
```

## Attach LRDB to host
1. Attach LRDB by running `Lua Attach` from Debug view.
2. Try to Step In. LRDB will automatically open `main.lua`.
