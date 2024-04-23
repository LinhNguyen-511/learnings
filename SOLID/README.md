# SOLID - decoupling code

## Single responsibility

- An object should have only 1 reason to change.
- A class should have exactly 1 job.

## Open-closed principle

- Entities (eg: classes, methods,...) should be open for extension, but closed for modification.
- Open for extension: simple to change the behaviour.
- Close for modification: without modifying the source code.
- Tips:
  - Move extensible behaviours to an interface and flip the dependencies.

## Liskov substitution principle

- Any implementations of an abstraction or interface should be substitutable anywhere that the abstraction is accepted.
- Interface functions should have return types.

## Interface segregation principle

- Client should not be forced to implement an interface that it doesn't use.

## Dependency inversion principle

- High level modules should not depend on low level modules, instead they should depend on abstractions.
- Low level code should depend on those abstractions as well.
- High level: doesn't concern about details.
- Low level: concerns with details and specifics.
- Dependency injection allows us to conform to this principle.
- Think about control and knowledge from the entity pov.
