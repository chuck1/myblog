## page was renamed from Departments/Engineering/ThermalEngineering/CoilFrameEtch
Describe Departments/Engineering/ThermalEngineering/Projects/CoilFrameEtch here.

{{{#!GraphViz dot
digraph CoilFrameMarking {
  file_coil -> circuit_generator
}
}}}

== Process to Implement ==

 * create left and right dxf for laser cutter
   * looks like currently use one drawing since they are mirrored parts, but this will not work for etch
 * determine programatically the offset from the origin to hole (0,0)
 * compile circuit generator into something that can be run by DA
 * set up the AutoCAD VBA so that it can be run by DA
 * program DA to
   * create the left and right dxf for laster cutter
   * run the circuit generator
   * open the dxf in AutoCAD and run the VBA using the circuit generator output text file
