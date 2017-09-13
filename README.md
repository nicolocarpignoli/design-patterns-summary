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
  
### Bridge
Decoupling an interface inheritance from implementation inheritance

* Use cases:  
  - Need of a run-time implementation binding
  - Separate development of interfaces from implementations
  - Need of sharing an implementation among multiple objects
  
 ### Decorator
Attach additional functionalities to objects at run-time (dynamically) with wrappers

* Use cases:  
  - Need of additional functionalities dynamically. Subclassing is static so is not an option
  - Need recursive additional functionalities
  
### Proxy
Provide a level of indirection between two objects

* Use cases:  
  - There is a hungry-resources objects that needs to be access-controlled. Need of an additional layer to control and manage         better such object
  - Instantiate such object only if client actually needs it
  - Protect the object from unnecessary complexity
  - ...
  
### Repository
Provide a level of indirection between logic and access to data

* Use cases:  
  - Need of separation of concerns between the logic layer and the data access layer
  - An additional layer lead to a better re-use of logic layer with different data(bases)
  - An additional layer provides space for logging, security management and other functionalities used from all the different data access layers

### Data Transfer Object (DTO)
Provide a model of data for a better usage from the repository side

* Use cases:  
  - Need of elaborate data with an higher level model, different from the database's one
  - Need of compute some logic/aggregation/filtering from data raw model
  
### Chain of Responsability
Provide a decoupled way to describe objects that manage a request-response behaviour. Each object can handle different requests: if one cannot handle a request it drives the responsability to another object

* Use cases:  
  - Need of handling a request with the best implementation available
  - Need of handling a new request at runtime with possible scenarios such as statically unknown request type or a runtime change of the available object for handle a specific request
  
  
### Iterator
Provide a standard way to iterate through different object's collections 

* Use cases:  
  - Need of standard behaviour for a sequential access through different object's collections. The idea is to treat the simple iteration action with a behaviour that is not related to the type of objects of a collection

### Memento
Used when it is required a way to restore an object state

* Use cases:  
  - Separation of concern: need of a specific separate component that handle the memorization of the state and the restore action 
  - Useful in every situation it is required a restoration of a state, such as an 'Undo' operation

WIP

## License
This project is released under MIT license as you can check in LICENSE.md file.
