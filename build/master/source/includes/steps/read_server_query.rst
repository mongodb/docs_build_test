.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Connect to your MongoDB instance.
   `````````````````````````````````

   .. include:: /includes/drivers_connect.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Connect to your MongoDB instance.
   `````````````````````````````````````````

   .. include:: /includes/drivers_connect.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Switch to the ``test`` Database
   ```````````````````````````````

   
   .. include:: /includes/bind_db.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Switch to the ``test`` Database
   ```````````````````````````````````````

   
   .. include:: /includes/bind_db.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Load more data into MongoDB.
   ````````````````````````````

   
   .. tip::
   
      If you have already :doc:`imported data into your database
      </server/import>` using :program:`mongoimport`, you can skip
      this step.
   
   Before you can write queries to extract data in a meaningful way, you'll need
   to add more data to your database. You can do that by running the ``insertMany()``
   nethod:
   
   .. include:: /includes/driver-example-query-14.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Load more data into MongoDB.
   ````````````````````````````````````

   
   .. tip::
   
      If you have already :doc:`imported data into your database
      </server/import>` using :program:`mongoimport`, you can skip
      this step.
   
   Before you can write queries to extract data in a meaningful way, you'll need
   to add more data to your database. You can do that by running the ``insertMany()``
   nethod:
   
   .. include:: /includes/driver-example-query-14.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Retrieve specific documents in a collection.
   ````````````````````````````````````````````

   
   You can retrieve specific documents from a collection by applying
   filter criteria.
   
   To specify filter criteria, pass a JSON document containing the
   criteria you are searching for to the ``find`` method.
   
   The following example illustrate using a status of "D" as criteria
   for narrowing a find on a collection.
   
   .. include:: /includes/driver-example-query-9.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Retrieve specific documents in a collection.
   ````````````````````````````````````````````````````

   
   You can retrieve specific documents from a collection by applying
   filter criteria.
   
   To specify filter criteria, pass a JSON document containing the
   criteria you are searching for to the ``find`` method.
   
   The following example illustrate using a status of "D" as criteria
   for narrowing a find on a collection.
   
   .. include:: /includes/driver-example-query-9.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Iterate over the results.
   `````````````````````````

   
   .. include:: /includes/iterate_all.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Iterate over the results.
   `````````````````````````````````

   
   .. include:: /includes/iterate_all.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">6</div></div>

   Check your results.
   ```````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that all records return have a status of "D".
   
   .. include:: /includes/results_read2.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 6: Check your results.
   ```````````````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that all records return have a status of "D".
   
   .. include:: /includes/results_read2.rst
   

