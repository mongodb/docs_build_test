.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Write an implied AND query with an "or" clause.
   ```````````````````````````````````````````````

   In the following example, the compound query document selects all
   documents in the collection where the ``status`` equals ``"A"``
   **and** *either* ``qty`` is less than 30 *or*
   ``item`` starts with the character ``p``:
   
   .. include:: /includes/driver-example-query-13.rst
   
   .. note::
   
      MongoDB supports regular expressions to
      perform string pattern matches.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Write an implied AND query with an "or" clause.
   ```````````````````````````````````````````````````````

   In the following example, the compound query document selects all
   documents in the collection where the ``status`` equals ``"A"``
   **and** *either* ``qty`` is less than 30 *or*
   ``item`` starts with the character ``p``:
   
   .. include:: /includes/driver-example-query-13.rst
   
   .. note::
   
      MongoDB supports regular expressions to
      perform string pattern matches.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Iterate over the results.
   `````````````````````````

   .. include:: /includes/iterate_all_noshellcursor.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Iterate over the results.
   `````````````````````````````````

   .. include:: /includes/iterate_all_noshellcursor.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Check your results.
   ```````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned.
   
   .. include:: /includes/results_read7.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Check your results.
   ```````````````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned.
   
   .. include:: /includes/results_read7.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

