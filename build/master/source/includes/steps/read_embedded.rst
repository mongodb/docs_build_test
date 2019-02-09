.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Retrieve specific documents in a collection based on the contents of an embedded document.
   ``````````````````````````````````````````````````````````````````````````````````````````

   
   If you wish to select documents that match all of the fields in an
   embedded JSON object, specify an exact match of the embedded document,
   including all of the fields and values in that embedded document in the
   order in which they appear in the collection.
   
   For example, the following query selects all documents where the
   ``size`` field equals the document ``{ "h" : 14, "w" : 21, "uom" : "cm"}``:
   
   .. include:: /includes/driver-example-query-15.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Retrieve specific documents in a collection based on the contents of an embedded document.
   ``````````````````````````````````````````````````````````````````````````````````````````````````

   
   If you wish to select documents that match all of the fields in an
   embedded JSON object, specify an exact match of the embedded document,
   including all of the fields and values in that embedded document in the
   order in which they appear in the collection.
   
   For example, the following query selects all documents where the
   ``size`` field equals the document ``{ "h" : 14, "w" : 21, "uom" : "cm"}``:
   
   .. include:: /includes/driver-example-query-15.rst
   

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
   more JSON documents returned. Note that the record matches the selection
   criteria exactly.
   
   .. include:: /includes/results_read3.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Check your results.
   ```````````````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that the record matches the selection
   criteria exactly.
   
   .. include:: /includes/results_read3.rst
   

