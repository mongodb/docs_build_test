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

   In this guide, you will update documents in a collection in the
   ``test`` database.
   
   .. include:: /includes/bind_db.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Switch to the ``test`` database.
   ````````````````````````````````````````

   In this guide, you will update documents in a collection in the
   ``test`` database.
   
   .. include:: /includes/bind_db.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Update a single document in the ``inventory`` collection.
   `````````````````````````````````````````````````````````

   To change a field value, MongoDB provides update operators
   to modify values. Some update operators, including
   will create the specified field if the field does not exist
   in the document.
   
   .. include:: /includes/driver-example-update-52.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Update a single document in the ``inventory`` collection.
   `````````````````````````````````````````````````````````````````

   To change a field value, MongoDB provides update operators
   to modify values. Some update operators, including
   will create the specified field if the field does not exist
   in the document.
   
   .. include:: /includes/driver-example-update-52.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Update multiple documents.
   ``````````````````````````

   The following operation updates all of the documents with
   ``quantity`` value less than 50.
   
   .. include:: /includes/driver-example-update-53.rst
   
   .. include:: /includes/driver-example-update-result.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Update multiple documents.
   ``````````````````````````````````

   The following operation updates all of the documents with
   ``quantity`` value less than 50.
   
   .. include:: /includes/driver-example-update-53.rst
   
   .. include:: /includes/driver-example-update-result.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

