## page was renamed from CharlesRymal/Projects/UniversalUnitDataStructure

We want to create a system that

 * can be adapted to a wide variety of unit types
 * can be adapted to work with different tools, since the tools we use could change over time

The best way to achieve these goals is to define a data structure for storing information about units. This data structure can simply be a collection of classes and raw data that defines a unit. This is independent of the tools that will be used to generate the data. It can be defined in a way that is independent of programming language or file format. This way, when we write new programs to design systems, or use new tools to create things like schematics, we can save time by continuing to use this file format. This will also make all our tools automatically compatible it they are all compatible with this data structure.

== Programming Libraries ==

 * C++
   * working directory: Linux virtual environment /home/crymal/backedup/git
   * repository: P:\git
 * C#
   * working directory: windows C:\...\Documents
   * repository: P:\git    

== Features ==

=== Object ===

An object is any dict in the data model.

=== Object Number ===

Any object can be given an object number.
An object number is used to reference an object from elsewhere is the data model.
Any set of objects that could be used in the same system must have object numbers assigned by a common source.
Anywhere in the data model where an object could go, an object reference can take its place.

If previously independent sets are combined, causing a situation where object numbers could be repeated, a routine can be used to modify the numbers in the second set.
Note that this could break object numbers references from a third set to the second set.

= Model Definition =

define the data model using C# class definitions. VS project "Consolidated Data Model", cdm.
