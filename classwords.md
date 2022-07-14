# Naming Database and Data Model Elements

The following conventions apply to database and data model elements.

## All Elements

- Use names that are as meaningful as possible given any length restrictions imposed by a particular technology
- Strive for consistent names within a model (extremely desirable), within a business area (highly desirable) and within the enterprise (ideal but may not be attainable in all cases)
- Use root words where possible but only if the root word is meaningful.  Dropping the suffix (-age, -ence, -ance, -ing, -ant, -ity, -any, -ive, -ary, -ony, -aty, -ory, -ation, -ment, -ed, -tion) will generally leave the root word.
- Do not use the plural form of words
- Do not use words such as who, what, when or where
- Do not use single words or combination of words that are commonly used as reserve words in data manipulation or definition languages
- Use articles and prepositions (such as **a, an, the** or **of**) and conjunctions (such **as** and or **or**) only on an exception basis
- Use only the characters A-Z, a-z and 0-9 for names.  Spaces can be used as word separators for logical model names.  Underscores are valid separators for physical names,  Special characters. including brackets. quotation makes, question marks, and slashes are not permitted in physical element names.  Dashes are allowed only in legitimately hyphenated words.
- Use a common diagramming notation

## Logical Model Elements

This section describes naming conventions for elements that will be defined during the logical modelling phase of application development.  The logical model should represent the world of the business area or function that is being modelled.  It is independent of the technology associated with an intended implementation.

### All Elements

- Identify all data elements (entities and attributes) and business rules; name them using business terminology
- Use complete words for logical data element names unless there is a common and easily identified acronym or other abbreviation.  For example, MAU is a standard abbreviation for Monthly Active Users.
- Separate words in a logical element name with a space.
- Provide definitions and examples for all logical data elements.

### Entities

- Use singular nouns or nominative phrases for entity names e.g. Employee rather than Employees
- Use single or multiple full-word descriptive names for entities; exceptions are allowed for the use of commonly used business acronyms and abbreviations.
- Name associative entities with a business name if possible; otherwise, name the associative entity with the names of the entities that are intersected, in a sensible order
  - Example of business term associative entity: If one entity is named ORDER and entity two is named PRODUCT, the associative might be called ORDER ITEM
  - Example of business term associative entity: If an Employee entity is associated with itself, a business term associated entity name might be Employee Reporting Hierarchy
  - Example of non-business term associative entity: CUSTOMER ADDRESS describes the connection of the CUSTOMER and ADDRESS entities
  - If there is no business term to describe the associative relationship, use the entity name followed by RELATED for an associative entity that associates an entity to itself i.e., it is recursive e.g., CUSTOMER RELATED

## Attributes

- Create an attribute to identify, qualify, classify, express the state of, or otherwise describe the properties of an entity
- Ensure that each occurence of an attribute within an entity has only one value
- Use multi-part names for attributes that range between 2 and 5 words according to the following pattern and examples

    {PrimeWordModifier(s)} PrimeWord {ClassWordModifier} ClassWord

    **Prime Word**: a word used to describe the element about which data is being collected.  The prime word should identify what the data element is.

    **Modifier Word(s)**: a word(s) used to further define the data element by modifying the prime and/or class words.  Any word that gives additional meaning to a prime or class word (usually adjectives or adverbs).

    **Class Word**: The list of Classwords in Appendix A identifies the general purpose classification of a data element.  The classword will describe the type of data element and serve to qualify the prime word.  Use a classword from the standard list.

## Relationships

- Identify relationships between all entities and represent business rules
- Name all relationships with a verb phrase

## Classwords

| Classword   | Datatype               | Notes                                                                                         | Example
|:----------- | :--------------------- | :-------------------------------------------------------------------------------------------- | :------------------------ |
| Amount      | Decimal(18,4)          | The quantity of monetary values                                                               | Credit Card Limit Amount  |
| Blob        | Binary Large Object    | A digital file such as a JPEG                                                                 | Passport Photo Blob       |
| Clob        | Character Large Object | A collection of character data used with Description or Text can't accomodate the size        | Security Key Clob         |
| Code        | Varchar(50)            | An assigned identifier that can be 'decoded' to make it meaningful                            | Department Code           |
| Count       | Integer                | An discrete indivisible number                                                                | Company User Count        |
| Date        | Date                   | A calendar date                                                                               | Birth Date                |
| Datetime    | Timestamp              | A date/time stamp                                                                             | User Create Datetime      |
| Description | Varchar(250)           | A textual description                                                                         | Project Description       |
| Identifier  | Integer                | A unique identifier                                                                           | Transaction Id            |
| Indicator   | Char(3)                | A binary (yes/no)                                                                             | Active Customer Indicator |
| Measure     | Decimal(18,4)          | A numeric usually with a unit of measure                                                      | Height Measure            |
| Name        | Varchar(100)           | A word or phrase that constitues the distinctive designation of a person plan thing or conept | City Name                 |
| Number      | Varchar(50)            | A noncomputable numeric value (may contain formatting)                                        | Drivers License Number    |
| Percent     | Decimal(9,4)           | A ratio between two values expressed as a part of 100                                         | Discount Percent          |
| Quantity    | Decimal(18,4)          | A comuptable numeric value                                                                    | Item Stock Quantity       |
| Rate        | Decimal(15,12)         | A ratio with multiple units of measure or a percentage rate                                   | Mortgage rate             |
| Text        | Varchar(1000)          | A textual phrase that does not fit name or description                                        | Customer Complaint Text   |
| Time        | Time                   | A clock time or time duration                                                                 | Shift End Time            |
| Value       | Varchar(100)           | A textual or noncomputable numeric denomination (discouraged)                                 | Trait Value               |
