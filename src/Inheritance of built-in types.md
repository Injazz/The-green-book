#Inheritance of built-in types
Even though, it's not explicitly shown, but most built-in types uses inheritance to derive some procs and variables from each other! There are 3 built-in types that are used as parents for everything else.

##`/atom`
The /atom object type is the parent of all mappable objects in the game. The types `/area`, `/turf`, `/obj`, and `/mob` are all derived from `/atom`. You should not create instances of `/atom` directly but should use `/area`, `/turf`, `/obj`, and `/mob` for actual objects. The `/atom` object type exists for the purpose of defining variables or procedures that are shared by all of the other "physical" objects. These are also the only objects for which verbs may be accessible to the user. 

##`/atom/movable`
The `/atom/movable` object type is the parent of all mappable objects that are capable of motion, it is also obvious that it's a child to the `/atom` type. The types `/obj` and `/mob` are derived from `/atom/movable`. You should not create instances of `/atom/movable` but should use `/obj` and `/mob` for actual objects. This object definition exists solely to define variables and procedures related to motion. 

##`/datum`
The datum object is the parent of all other data types in DM (with exceptions listed below). That means that the variables and procedures of /datum are inherited by all other types of objects. When you define a new "top level" object, if you do not specify a parent_type, it defaults to /datum. 
The following types **aren't** `/datum` children: `/world`, `/client`, `/list` , and `/savefile`.