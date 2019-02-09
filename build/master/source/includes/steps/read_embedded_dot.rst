.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Retrieve specific documents in a collection with dot notation.
   ``````````````````````````````````````````````````````````````

   
   If you wish to select documents that exactly match just one of the
   fields in an embedded JSON object, use  :ref:`dot notation <document-dot-notation>`.
   (``"field.nestedField"``).
   
   When querying using :ref:`dot notation <document-dot-notation>`., the field and nested field names must be
   inside quotation marks.
   
   The following example selects all documents where the field ``uom``
   nested in the ``size`` field equals ``"in"``:
   
   .. include:: /includes/driver-example-query-17.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Retrieve specific documents in a collection with dot notation.
   ``````````````````````````````````````````````````````````````````````

   
   If you wish to select documents that exactly match just one of the
   fields in an embedded JSON object, use  :ref:`dot notation <document-dot-notation>`.
   (``"field.nestedField"``).
   
   When querying using :ref:`dot notation <document-dot-notation>`., the field and nested field names must be
   inside quotation marks.
   
   The following example selects all documents where the field ``uom``
   nested in the ``size`` field equals ``"in"``:
   
   .. include:: /includes/driver-example-query-17.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Iterate over the results.
   `````````````````````````

   .. include:: /includes/iterate_all.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Iterate over the results.
   `````````````````````````````````

   .. include:: /includes/iterate_all.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Check your results.
   ```````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that the result record has a ``uom`` of ``in``.
   
   .. include:: /includes/results_read4.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Check your results.
   ```````````````````````````

   
   If you have loaded data into your test database, you will see one or
   more JSON documents returned. Note that the result record has a ``uom`` of ``in``.
   
   .. include:: /includes/results_read4.rst
   
   .. include:: /includes/drivers_close_connection.rst
   

