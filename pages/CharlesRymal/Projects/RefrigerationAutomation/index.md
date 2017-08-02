## page was renamed from People/CharlesRymal/Projects/RefrigerationAutomation
At a high level we want to create a system that
 * can be adapted to a wide variety of unit types
 * can be adapted to work with different tools, since the tools we use could change over time

The best way to achieve these goals is to define a data structure for storing information about units. This data structure can simply be a collection of classes and raw data that defines a unit. This is independent of the tools that will be used to generate the data. It can be defined in a way that is independent of programming language or file format. This way, when we write new programs to design systems, or use new tools to create things like schematics, we can save time by continuing to use this file format. This will also make all our tools automatically compatible it they are all compatible with this data structure.

== Goal ==

 * Create BOM for purchasing 
 * Create a schematic with line sizes and part numbers identified
   * To be used by piping team to create piping model
 * Automate selection of line sizes and components

== Function Outline ==

 * Inputs
   * RBE file
   * P&ID drawing file for each circuit
     * copy a template with a given type of condenser, number of liquid line splits, and presence of hot gas bypass
     * make job-specific modifications
     * The drawing contains no part numbers or line sizes.
     * The drawing only contains information about the number of liquid lines and the presence of certain types of components.
 * for each circuit
   * export excel data from the data manager in the P&ID drawing
   * using C# program and reading the excel file, traverse the schematic
   * liquid line traversal
     * find the liquid line leaving the condenser
     * follow the liquid line downstream, recursively following each liquid line split
     * stop when each liquid line reaches the evaporator
     * the program should now know the fraction of the full capacity that is carried in each liquid line split
     * the program can now size each liquid line size and components based on that capacity
   * do a similar process for the hot gas bypass lines
