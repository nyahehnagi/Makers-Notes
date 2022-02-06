# Domain Modelling

What is an object 
  - Stored in a program
  - Represents a logical entity
  - Has capabilities, functionality
  - Collection of properties and methods
  - Complex


* Why do we use multiple objects in our programs
    - Objects can be shared
    - Simulating some domain
    - allow to store discrete data
    - conceptulise multiple versions of a class

* why do we use multiple classes in our programs
    - Breaking features up
    - Maintenance
    - Different classes have different properties
    - Single Responsibility Principle
    - Encapsulation, we don't want all methods to be public
    - interaction between objects


Domain Modelling Workshop

https://github.com/makersacademy/skills-workshops/tree/main/object_oriented_programming/domain_modelling_alternative


Eventually got my stubs working for the SMS Client in the Takeway Challenge.

The key element was using my doubles correctly.
~~~~
  let(:failed_code) { double(:message, :error_code => 1) }
  let(:failed_messages) { double(:messages, :create => failed_code) }
  let(:failed_twilio_client) { double(:twilio_client, :messages => failed_messages) }

  let(:error_code) { double(:message, :error_code => nil) }
  let(:messages) { double(:messages, :create => error_code) }
  let(:succesful_twilio_client) { double(:twilio_client, :messages => messages) }
~~~~

Note that I am nesting the use of the doubles !
