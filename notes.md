Data modeling is a game of abstraction.

A good data model

- captures all the data the system needs
- captures ONLY the data the system needs
- reflects reality
- is flexible, can evolve with the system
- guarantees data integrity without sacrificing performance
- is driven by the way we access data in the system

Components

- entities: the nouns, resources in REST terminology.
- properties: information we need to track about the entity.
- relationships: how they relate to each other.

Workflow

- identify entities -----> tables
- identify properties for each entity -----> columns
- identify relationships between two entities at a time -----> foreign key

Ideally you want to get to the 3NF (Third normal form).

Types of Relationships

- one to one
- one to many <--< this is it
- many to many <-- a trick, smoke and mirrors

Immunization Tracker

- patient and staff point of view

patient input info and not change it

staff access all change some information

track children imm.... records (parents, schools (future), doctor's office)

Entities

- patient (any user will be a patient)
  - basic contact information
  - dependents
- immunization <-- transactional (event occurs in time between two entities)
- vaccine
- appointments

* employees
* clinics

several employees work at the same clinic ---> a clinic has several employees
the same employee can work in different clinics

Mantras

- every table has a one and only one primary key (it could be made up of more than one colum <- composite keys)
- one to many relationships there is a FK involved
- the FK goes in the many side
- for a many to many we need a third table
- a many to many table can have extra information about the event