Makefile and make
=================

- `make` is generally used to compile large programs, based on set of rules written in a `Makefile`
- Generally, it is used to automate a set of tasks, where some files need to be updated when other change or when some tasks need to be run .
- `Makefile` is a collection of rules that is used by `make` to compile the program.

Goal
----

- Goals are target that `make` will strive to update. By default, the first target in the `Makefile` is the _goal_

Rules
-----

- The `rule` is written as follows

```make
target ... : prerequisites ....
<TAB>recipe
<TAB>...
```
- `target` is usually the name of __one or more__ files generated from prerequisites. It can also be an action like `clean`
- `prerequisites` are one or more files on which the target is dependent. If any of the prerequisites has a later modification time than the target, the recipe is executed to generate the target. There could be a target without any prerequisites.
- `recipe` is a set of one or more shell commands executed by `make` to generate the target file from the prerequisites.
- __Note__ - the `TAB` character on each recipe line is critical. It cannot be space, and is difficult to spot, so take care of this.






Variables
---------

- https://www.gnu.org/software/make/manual/html_node/Variables-Simplify.html#Variables-Simplify






References
----------
- [Make Online Book]
- [Quick Reference]
- [Special Targets]



[Make Online Book]: https://www.gnu.org/software/make/manual/html_node/index.html#toc-Overview-of-make
[Quick Reference]: https://www.gnu.org/software/make/manual/html_node/Quick-Reference.html#Quick-Reference
[Special Targets]: https://www.gnu.org/software/make/manual/html_node/Special-Targets.html#Special-Targets
[Phony Targets]: https://www.gnu.org/software/make/manual/html_node/Phony-Targets.html#Phony-Targets




