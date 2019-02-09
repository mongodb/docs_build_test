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

   In this guide, you will delete documents in a collection in the
   ``test`` database.
   
   .. include:: /includes/bind_db.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Switch to the ``test`` database.
   ````````````````````````````````````````

   In this guide, you will delete documents in a collection in the
   ``test`` database.
   
   .. include:: /includes/bind_db.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Delete a single document.
   `````````````````````````

   The following operation deletes the **first** document with ``status``
   equal to ``D``:
   
   .. include:: /includes/driver-example-delete-58.rst
   
   .. include:: /includes/driver-example-delete-result.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Delete a single document.
   `````````````````````````````````

   The following operation deletes the **first** document with ``status``
   equal to ``D``:
   
   .. include:: /includes/driver-example-delete-58.rst
   
   .. include:: /includes/driver-example-delete-result.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Delete multiple documents.
   ``````````````````````````

   The following operation deletes *all* of the documents in the
   specified ``inventory`` collection with ``status`` equal to ``A``:
   
   .. include:: /includes/driver-example-delete-57.rst
   
   .. include:: /includes/driver-example-delete-result.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Delete multiple documents.
   ``````````````````````````````````

   The following operation deletes *all* of the documents in the
   specified ``inventory`` collection with ``status`` equal to ``A``:
   
   .. include:: /includes/driver-example-delete-57.rst
   
   .. include:: /includes/driver-example-delete-result.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

