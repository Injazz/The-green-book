# Installation
If you're reading this, you probably have [BYOND] installed already. When you install it to play games, you also install some other programs:

[BYOND]: http://www.byond.com/download/

1. Dream Maker
2. Dream Daemon
3. Dream Seeker

## Dream Maker
The first is what you'll use to code. It's the IDE which you use to write code, compile and eventually run for testing purposes (although, for large projects, it's suggested to use Dream Daemon to run the code, since it's how you'd run it in a production environment).

By default, it is located in BYOND bin folder, accessible from wherever you installed byond (normally, Program Files(x86) ). 

Once opened, you will see a window separated in three parts, normally.

### The file tree
The rectangle on the left with a white background is the file tree. It basically shows the files of your project the IDE cares about. This means, all DM related files (.dm, .dmi, .dme, dmf, dms, dmm), images and sounds. In particular, .dm and .dmm files will have a small box on the left of the filename, which you can mark. If there is a checkmark in said box, then the file is included in the .dme, which means it will be compiled when the .dme is compiled, otherwise it will be ignored.
If you doubleclick a file, the IDE will attempt to open it in...

### The working area
Aka the big gray area on the right, when you open a file it'll display it in this area. For .dm files, it'll show the file (text) contents, with syntax highlighting and the ability to also display indentation and line number, based on preferences. After writing some code, you'll have to compile it to be able to run it. You can do it from the `Build` tab top left, or with the `CTRL+K` hotkey. Compiling will lead to some text being displayed in...

### The compiler output window
Aka the white rectangle on the bottom. When compiling code, info will be outputted in this part, in particular compile errors. If an error happens, you can doubleclick the line to automatically open the file containing the line, with said line highlighted. If no errors show up, the output will ultimately save a special .dmb file, which is basically the executable. Once you get this, you can proceed to run your code and see how it behaves.

## Dream Daemon
When you build the .dmb executable, you can either simply run your code directly from Dream Maker from the `Build` tab, or host a server through Dream Daemon. This is usually used for production stage, when you want to host a game for other people to be able to join. The interface is pretty simple, you feed it the .dmb file, eventually set a Port if you port forwarded one, choose whether your server should be visible to anyone or not, and specify the security level. Security level is for certain procs able to access system commands, such as `shell()`. Some games may require you to allow those commands, such as Space Station 13, to work properly. To do so, set it to Trusted. Otherwise, if you want to block said calls, use Safe. More about this will be discussed in future.

## Dream Seeker
This is simply the program you use to connect to servers. If you've ever played a game on BYOND, this is what you're running to play it. 

Now that you know the basics, you can proceed to your first Hello World program.