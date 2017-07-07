# design-patterns-summary

## Gang of Four's Design Pattern Summary

### Adapter
Used when you need to connect two different interfaces without modifying them

* How:
* Use cases: 
- Integrating legacy code
- Integrating libraries (e.g. when there's no chance to modify source code)
- You want to create a base interface to connect interfaces you don't know yet
- You want to hide specific method signatures and expose simple methods
- ..

### Abstract Factory
Used for create familiy of objects with separation of the creation logic from the rest of the code, withouth specifying concrete implementation of objects

* How:
* Use cases: 
- Need for a separate logic for creation of objects
- Create familiy of related objects in a consistent way
- Hiding implementation of family objects (specific factories) and hiding client access to specific objects
- Need for coherence between objects created from the same factory
- Easy switching between different factories for the client
- ..

### Factory Method
Used when you need to create (single) objects hiding creation logic and let subclasses choose the implementation

* How:
* Use cases:  
- Need for a separate logic for creation of objects (Separation of concerns principle)
- Need for hiding creation logic and creation resources
- Centralize where we are creating objects
- Less duplicated code
- ..


## License
This project is released under MIT license as you can check in LICENSE.md file.
