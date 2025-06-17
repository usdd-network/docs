# OSM

### **Purpose**

It ensures that new price values propagated from the Oracles are not taken up by the system until a specified delay has passed.

### Key Responsibilities

* Periodically feeds a delayed price into the system for a particular collateral type.

### Key Methods

* `peek()`\
  Returns the current feed value and a boolean indicating whether it is valid.
* `read()`\
  Returns the current feed value; reverts if it was not set by some valid mechanism.
* `peep()`\
  Returns the next feed value (i.e. the one that will become the current value upon the next `poke()` call), and a boolean indicating whether it is valid.
