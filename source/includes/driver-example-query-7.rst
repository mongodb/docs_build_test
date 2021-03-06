.. tabs-drivers::

   tabs:
     - id: shell
       content: |
         .. code-block:: javascript

            myCursor = db.inventory.find( {} )

     - id: compass
       content: |

         Select the :guilabel:`test` database in the list of available databases.

         Then select the :guilabel:`inventory` collection to view all documents in the collection.

     - id: python
       content: |
         .. literalinclude:: /driver-examples/test_examples.py
            :language: python
            :dedent: 8
            :start-after: Start Example 7
            :end-before: End Example 7

     - id: motor
       content: |
         .. literalinclude:: /driver-examples/test_examples_motor.py
            :language: python
            :dedent: 8
            :start-after: Start Example 7
            :end-before: End Example 7

         For completeness, this is how you might wrap the call and run it in an asyncio loop:

         .. code-block:: python
            
            async def do_find():
                cursor = db.inventory.find({})
                async for doc in cursor:
                   pprint.pprint(doc)

            loop = asyncio.get_event_loop()
            loop.run_until_complete(do_find())

     - id: java-sync
       content: |
 
         First you will need to create the MongoCollection object you would like to query against.

         .. code-block:: sh

            MongoCollection<Document> collection = db.getCollection("inventory");
          
         Then query the collection for all documents by passing an empty document
         to the find() method.
         
         .. literalinclude:: /driver-examples/DocumentationSamples.java
            :language: java
            :dedent: 8
            :start-after: Start Example 7
            :end-before: End Example 7

     - id: nodejs
       content: |
         .. literalinclude:: /driver-examples/examples_tests.js
            :language: javascript
            :dedent: 8
            :start-after: Start Example 7
            :end-before: End Example 7

     - id: csharp
       content: |
         .. literalinclude:: /driver-examples/DocumentationExamples.cs
            :language: c#
            :dedent: 12
            :start-after: Start Example 7
            :end-before: End Example 7

     #- id: php
     #  content: |
     #    .. literalinclude:: /driver-examples/DocumentationExamplesTest.php
     #       :language: php
     #       :dedent: 8
     #       :start-after: Start Example 7
     #       :end-before: End Example 7

     #- id: perl
     #  content: |
     #   .. literalinclude:: /driver-examples/driver-examples.t
     #       :language: perl
     #       :dedent: 4
     #       :start-after: Start Example 7
     #       :end-before: End Example 7

     #- id: ruby
     #  content: |
     #    .. literalinclude:: /driver-examples/shell_examples_spec.rb
     #       :language: ruby
     #       :dedent: 8
     #       :start-after: Start Example 7
     #       :end-before: End Example 7

     #- id: scala
     #  content: |
     #    .. literalinclude:: /driver-examples/DocumentationExampleSpec.scala
     #       :language: scala
     #       :dedent: 4
     #       :start-after: Start Example 7
     #       :end-before: End Example 7


