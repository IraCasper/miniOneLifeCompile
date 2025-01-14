# miniOneLifeCompile

 Minimal scripts to compile 2HOL/OHOL client, server and editor

## TLDR Usage

Get WSL (Windows Subsystem for Linux) by enabling it in "Apps & features", and then in the WSL shell run the line below to compile and start the game client:

```bash
./buildFromScratch.sh
```

## Compiling (and running) the Server

```bash
./cleanOldBuildsAndCaches.sh
./server.sh
```

## Compiling the Editor

```bash
./cleanOldBuildsAndCaches.sh
./getEditorDependencies.sh
./editor.sh
```

## Quick Recompiling the Game Client

After you made changes to the client code, just run this, and it will start the new client as well:

```bash
./compile.sh
```

## Start Server (Without Recompiling)

```bash
./runServer.sh
```

## Other Platforms

The scripts cross-compile the client and editor for Windows on Linux, and compile the server for Linux by default. 

To compile the client and editor for Linux:

(Note: running graphical apps on WSL requires additional third-party apps, e.g. Xming, to work)

```bash
./cleanOldBuildsAndCaches.sh
./compile.sh 1
```

```bash
./cleanOldBuildsAndCaches.sh
./editor.sh 1
```

To cross-compile the server for Windows on Linux:

```bash
./cleanOldBuildsAndCaches.sh
./server.sh 5
```

## Note 

The scripts expect folder structure as below, you may want to clone this repo within a root folder:
```
root/
├── miniOneLifeCompile/
├── OneLife/
├── OneLifeData7/
├── minorGems/
└── output/
```

## More Info

This is meant to be minimal, if you want more info:

[Defalt's TwoLifeXcompile](https://github.com/Defalt36/TwoLifeXcompile)

[OneLifeXcompile](https://github.com/Joriom/OneLifeXcompile) (where the makefile in this repo for cross-compiling for Windows on Linux came from)

[Jason's compiling note](http://onehouronelife.com/compileNotes.php?nocounter=1)

[Note on cross-compiling the editor](https://github.com/jasonrohrer/OneLife/blob/dba27afbcee804026962f9fae319540f45fd6e42/documentation/devProcess/mingwNotes.txt)

[Note on compiling the editor and server](https://github.com/jasonrohrer/OneLife/blob/dba27afbcee804026962f9fae319540f45fd6e42/documentation/EditorAndServerBuildNotes.txt)

[Some old scripts to compile 2HOL](https://github.com/twohoursonelife/2HOL)

[Hetuw's compile scripts](https://github.com/hetuw/OneLife/tree/master/scripts/hetuwScripts)
