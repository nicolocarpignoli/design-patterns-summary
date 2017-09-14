# design-patterns-summary

## A summary of most used Gang of Four's Design Pattern and more

This is a design pattern summary made by me. Its aim is to provide a quick reference for the most used design patterns. You can quickly see what every pattern is about and the most important use cases selected by me. 

When you have found one or more pattern that suited well for you on solving some of your problems, you can go deep in tech with the implementation examples. Some interesting (free) web references for the implementations:

* https://www.tutorialspoint.com/design_pattern/design_pattern_overview.htm
* https://sourcemaking.com/design_patterns


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
  - Create families of related objects in a consistent way
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

### Observer 
A fundamental pattern used for manage one-to-many communication. The architecture is structured in a way that requires that every observer is registered to an object 'to observe', on each - or specific - state changes. When a change occurs every observer gets the information with callback functions.

* Use cases:  
  - Separation of concerns between object to observe and observers. The one-to-many communication leds to hard decoupling betewwn such actors.
- It is possible to manage different behaviour: every observer can specify which property to observe and how to respond to the eventual changes
- It is a fundamental way to handle event communication. Callbacks make the communication asynchronous, so each observer can continue with its flow

### MVC Pattern 
Another fundamental pattern that means Model View Controller. Its main goal is to provide separation of concerns between components of a system. The system is divided in three main macro-components: a model, that represent the data and the way we have modeled reality in our system; a controller, where the logic can drive model information to the view, treating them and elaborating them first. The view part has the only responsability of visualizing the data provided by the controller.

* Use cases:  
  - Separation of concerns
  - Good way to organize projects that have a 'view' part that it's only suited for visualizing data (e.g. for web applications or applications with a UI)
  - The component separation led to a better manutebility, testing, scalability and modularity of code


WIP

## License
This project is released under MIT license as you can check in LICENSE.md file.
