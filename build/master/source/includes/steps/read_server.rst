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

   Switch to the ``test`` database.
   ````````````````````````````````

   
   Switch to the database you wish to query. In this case we will be
   using ``test``.
   
   .. include:: /includes/bind_db.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Switch to the ``test`` database.
   ````````````````````````````````````````

   
   Switch to the database you wish to query. In this case we will be
   using ``test``.
   
   .. include:: /includes/bind_db.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Retrieve all documents in the ``inventory`` collection.
   ```````````````````````````````````````````````````````

   .. include:: /includes/find_all.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Retrieve all documents in the ``inventory`` collection.
   ```````````````````````````````````````````````````````````````

   .. include:: /includes/find_all.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Iterate over the results.
   `````````````````````````

   .. include:: /includes/iterate_all_noshellcursor.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Iterate over the results.
   `````````````````````````````````

   .. include:: /includes/iterate_all_noshellcursor.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Check your results.
   ```````````````````

   
   If you loaded the data from :doc:`/server/insert`, you should
   see output that resembles the following:
   
   .. include:: /includes/results_read1.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Check your results.
   ```````````````````````````

   
   If you loaded the data from :doc:`/server/insert`, you should
   see output that resembles the following:
   
   .. include:: /includes/results_read1.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

