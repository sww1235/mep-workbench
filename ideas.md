# Ideas

Use container object that can hold other geometry objects like parts and bodies to add mep functionality.

General idea is to give objects connection points which carry the logical data like connection type, voltage, liquid, temperature, etc. These connection points can be associated with specific parts of an objects geometry and can have parameters driven by the associated geometry. For example, the size of a pipe or duct would be represented by the size of the physical hole on the object.

The connection points can be grouped into systems and system classes (maybe subclasses).

The other main object would be the connectors between connection points. These would be only point to point links, with the assumption that a user would define a junction object to create intersections.

The connectors can also have both physical geometry and logical data associated.

Ideally, the physical geometry could be at least partially auto generated based on material properties and physical sizing (maybe even generating transitions automatically)

The connectors can have auto-placement algorithms assigned that, ideally, can recognize walls and other obstacles.

Classes would represent the overall usage of a connection point, so separating liquid from gas, and electrical from liquid.

Systems would represent an individual collection of devices and would be mostly user defined. This allows for granular systems for electrical, hvac, plumbing etc.

The idea is to allow users to easily define new classes and systems and be very flexible around what the systems represent.

Want to allow for lots of reporting and schematic generation. Panel schedules, etc.

Connection points would only represent one system (may need to change this) and connectors and objects with connection points could be categorized into one or multiple system classes so you can't mix up connection points of different systems.

Need to be able to draw 2d plan diagrams automatically,but allow them to be modified. Freecad philosophy of 3d first.

Need to be able to have multiple different geometries associated with each object, so can show simplified objects during planning phase and photorealistic objects during rendering.

The dream of this workbench is to be able to photorealistically render MEP systems with accurate conduit/pipe/wire locations, sizing etc, but also be able to run FEM, HVAC, electrical load, etc calculations and generate reports and schedules at the end.

As a related effort, there would be a curated repo of common objects that users could use, and also see how they were built so as to create new objects.
