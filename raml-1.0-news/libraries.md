<h3>What's new in RAML 1.0</h3>

Libraries favor reuse of predefined sets of data-types, resourceTypes, traits, security, schemas, etc.
Here is an illustration of a the use of libraries in RAML 1.0
<pre>
#%RAML 1.0
title: A CRUD API for training Modules and Curriculae
mediaType: application/json

uses:
  - Core: !include libraries/types/core.raml
  - Module:   !include libraries/types/module.raml
  - Curriculum:  !include libraries/types/curriculum.raml
  - CRUD:   !include libraries/resourceTypes/crud.raml

/modules:
  description: All the modules
  type:
    CRUD.collection:
      typename: User.full
      typename-new: User.new
</pre>