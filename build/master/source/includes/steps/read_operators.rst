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

   Switch to the database you wish
   to query. In this case we will be using
   ``test``.
   
   .. include:: /includes/bind_db.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Switch to the ``test`` database.
   ````````````````````````````````````````

   Switch to the database you wish
   to query. In this case we will be using
   ``test``.
   
   .. include:: /includes/bind_db.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Select documents using the less-than operator.
   ``````````````````````````````````````````````

   The following example retrieves all documents from the inventory
   collection where the ``size.h`` field is less than 15. MongoDB uses
   :ref:`dot notation <document-dot-notation>` to specify fields within
   embedded documents. ``size.h`` refers to the ``h`` field in the
   ``size`` document.
   
   .. include:: /includes/driver-example-query-18.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Select documents using the less-than operator.
   ``````````````````````````````````````````````````````

   The following example retrieves all documents from the inventory
   collection where the ``size.h`` field is less than 15. MongoDB uses
   :ref:`dot notation <document-dot-notation>` to specify fields within
   embedded documents. ``size.h`` refers to the ``h`` field in the
   ``size`` document.
   
   .. include:: /includes/driver-example-query-18.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Iterate over the results.
   `````````````````````````

   .. include:: /includes/iterate_all.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Iterate over the results.
   `````````````````````````````````

   .. include:: /includes/iterate_all.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Check your results.
   ```````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that the records have a height ("size.h") of
   less than 15.
   
   .. include:: /includes/results_read5.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Check your results.
   ```````````````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that the records have a height ("size.h") of
   less than 15.
   
   .. include:: /includes/results_read5.rst
   

