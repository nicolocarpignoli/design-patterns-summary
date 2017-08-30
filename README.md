# design-patterns-summary

## A summary of most used Gang of Four's Design Pattern and more

### Adapter
Used when you need to connect two different interfaces without modifying them

* Use cases: 
  - Integrating legacy code
  - Integrating libraries (e.g. when there's no chance to modify source code)
  - You want to create a base interface to connect interfaces you don't know yet
  - You want to hide specific method signatures and expose simple methods

### Abstract Factory
Used for create familiy of objects with separation of the creation logic from the rest of the code, withouth specifying concrete implementation of objects

* Use cases: 
  - Need for a separate logic for creation of objects
  - Create familiy of related objects in a consistent way
  - Hiding implementation of family objects (specific factories) and hiding client access to specific objects
  - Need for coherence between objects created from the same factory
  - Easy switching between different factories for the client

### Factory Method
Used when you need to create (single) objects hiding creation logic and let subclasses choose the implementation

* Use cases:  
  - Need for a separate logic for creation of objects (Separation of concerns principle)
  - Need for hiding creation logic and creation resources
  - Centralize where we are creating objects
  - Less duplicated code
  - ..
  
### Singleton
Used for having a single instance of a specific object in a software system

* Use cases:  
  - Need of a single instance for coherence and avoid conflicts about behaviour and object state
  - Need of a single/central object used by a large set of other instances (a Logger for example); in these cases it can avoid a significant dependecy injection effort
  
WIP

## License
This project is released under MIT license as you can check in LICENSE.md file.
