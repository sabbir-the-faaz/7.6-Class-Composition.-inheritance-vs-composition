# 7.6-Class-Composition.-inheritance-vs-composition
7.6 Class Composition. inheritance vs composition
 let's discuss the provided code in the context of inheritance and composition.

**Inheritance**:
- Inheritance is about creating new classes that are based on existing classes, inheriting their attributes and behaviors. 
- In the given code, there's no explicit inheritance relationship defined between the classes.
- If there was a need for a subclass of `car`, let's say `SportsCar`, which had additional attributes or methods compared to a regular `car`, you could achieve this through inheritance. For example:

```python
class SportsCar(car):
    def __init__(self) -> None:
        super().__init__()
        self.turbo = True
```
In this case, `SportsCar` inherits from `car`, acquiring its properties like `engine` and `driver`.

**Composition**:
- Composition involves constructing complex objects by combining simpler ones.
- In the provided code, the `car` class is composed of instances of the `Engine` and `driver` classes.
- This is evident in the `car` class's `__init__` method where instances of `Engine` and `driver` are created and assigned as attributes.
- This composition implies that a `car` has an `Engine` and a `driver`, representing a "has-a" relationship.

```python
class car:
    def __init__(self) -> None:
        self.engine = Engine()  # Composition: Car has an Engine
        self.driver = driver()  # Composition: Car has a driver
```

In summary, the given code demonstrates composition, as the `car` class is composed of instances of other classes (`Engine` and `driver`). There's no explicit inheritance relationship defined in the provided code snippet. If there were additional classes that needed to inherit from existing ones, inheritance could be utilized to establish an "is-a" relationship between the classes.
