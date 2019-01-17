# Built-in Object Types
Dream Maker has several object types already implemented for you to use. You can straight redefine existing object's variables and procs, as well as you can inherit this type with your own object and set inherited variables and procs as you please, or you can add additional variables and procs straight to built-in object types (such behavior in other languages called [monkey patch](https://en.wikipedia.org/wiki/Monkey_patch)! Let's see how it works on following example:

```dm
//atom is a built-in type, but you can define it!
/atom 
	layer = 1
	//var/layer = 1 //WON'T COMPILE - duplicate definition! Uncomment this to try it yourself!
	var/example_variable = 1 //will be added to all /atom objects
```

Notice that we don't use `var/` since `layer` is already built-in variable that defined right in the game engine, you won't find it's definition in your game code.

You can redefine built-in procs, as well as adding your own procs to built-in type:
```dm
/atom/New(loc, ...)  //you can redefine built-in proc
	world << "Hello, i'm atom!"

/*
/atom/proc/New(loc, ...) //WON'T COMPILE - duplicate definition! Uncomment this to try it yourself!
	world << "Oh no, we won't see this!"
*/

/atom/proc/example_proc() //this proc will be available for all /atom objects
	world << "We called an example proc on atom!"
```

Now let's use the same proc we used in our `Hello World` program and see some input:
```dm
/mob/Login()
	var/atom/A = new /atom(loc) //loc is a built-in variable for /atom
	world << A.layer //will display 1, since we assigned this value to it
	world << A.example_variable //will display 1
	world << A.invisibility //Even though there is no definition for invisibility in our code, it would display 0, since invisibility is also a built-in variable and has a default value of 0!
```

Notice that `/mob` is a built-in object, which inherits `/atom` (we'll talk about this inheritance in the next chapter) so it can use `loc` variable, which actually belongs to `/atom`! Also you probably understand now that `Login()` is a built-in proc for `/mob`, right? Right.
Full list of built-in object types with var and proc definitions can be found [here](http://www.byond.com/docs/ref/index.html).
