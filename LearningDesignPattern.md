
 # Design Patterns 
 
 1. Creational : Related to creation of objects.
 2. Structural 
 3. Behavioural 
 
 ## Types Of Creational
 1. Singelton Pattern  
 2. Builder Pattern
 3. Prototype Pattern 
 4. Factory 
 5. AbstractFactory 
 
 Things to Learn : 
 1. Usages of that Pattern. 
 2. Implementation.
 3. Pitfall of it compare to others.
 4. When to use a particular Pattern. 
 
 ## Singelton
 1. Usage : 
      a. Only one instance created.
      b. Guarantees control of a resource. 
      c. Lazily Loaded. (When Needed)
 2. Examples : Spring Beans (By Default Singleton) , Logger
 3. In Singelton, class is not static because then it will not be thread safe, it has a private constructor and a getInstance static method because object cannot be made and only one instance is required. If <b> parameters </b> need to be given for constructor then it will not be singelton pattern. 
 4. 
