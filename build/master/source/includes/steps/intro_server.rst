.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Define Your Data Set
   ````````````````````

   
   When setting up a data store, your first task is to answer the
   question: "What data would I like to store and how do the fields
   relate to each other?".
   
   This guide uses a hypothetical inventory database to track items and
   their quantities, sizes, tags, and ratings.
   
   Here is an example of the types of fields you might wish to capture:
   
   .. list-table::
      :header-rows: 1
      :widths: auto
      :class: guide-tablenate
   
      * - name
        - quantity
        - size
        - status
        - tags
        - rating
   
      * - journal
        - 25
        - 14x21,cm
        - A
        - brown, lined
        - 9
   
      * - notebook
        - 50
        - 8.5x11,in
        - A
        - college-ruled,perforated
        - 8
   
      * - paper
        - 100
        - 8.5x11,in
        - D
        - watercolor
        - 10
   
      * - planner
        - 75
        - 22.85x30,cm
        - D
        - 2019
        - 10
   
      * - postcard
        - 45
        - 10x,cm
        - D
        - double-sided,white
        - 2
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Define Your Data Set
   ````````````````````````````

   
   When setting up a data store, your first task is to answer the
   question: "What data would I like to store and how do the fields
   relate to each other?".
   
   This guide uses a hypothetical inventory database to track items and
   their quantities, sizes, tags, and ratings.
   
   Here is an example of the types of fields you might wish to capture:
   
   .. list-table::
      :header-rows: 1
      :widths: auto
      :class: guide-tablenate
   
      * - name
        - quantity
        - size
        - status
        - tags
        - rating
   
      * - journal
        - 25
        - 14x21,cm
        - A
        - brown, lined
        - 9
   
      * - notebook
        - 50
        - 8.5x11,in
        - A
        - college-ruled,perforated
        - 8
   
      * - paper
        - 100
        - 8.5x11,in
        - D
        - watercolor
        - 10
   
      * - planner
        - 75
        - 22.85x30,cm
        - D
        - 2019
        - 10
   
      * - postcard
        - 45
        - 10x,cm
        - D
        - double-sided,white
        - 2
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Start Thinking in JSON
   ``````````````````````

   
   While a table might seem like a good place to store data, as you can
   see from the example above, there are fields in this data set that
   require multiple values and would not be easy to search or display if
   modeled in a single column (for example -- ``size`` and ``tags``).
   
   In a SQL database you might solve this problem by creating a
   relational table.
   
   In MongoDB, data is stored as documents. These documents are stored in
   MongoDB in ``JSON`` (JavaScript Object Notation) format. JSON documents support
   embedded fields, so related data and lists of data can be stored with
   the document instead of an external table.
   
   JSON is formatted as name/value pairs. In JSON documents, fieldnames
   and values are separated by a colon, fieldname and value pairs are
   separated by commas, and sets of fields are encapsulated in "curly
   braces" ({}).
   
   If you wanted to begin to model one of the rows above, for example
   this one:
   
   .. list-table::
      :header-rows: 1
      :widths: auto
      :class: guide-tablenate-odd
   
      * - name
        - quantity
        - size
        - status
        - tags
        - rating
   
      * - notebook
        - 50
        - 8.5x11,in
        - A
        - college-ruled,perforated
        - 8
   
   You might start with the ``name`` and ``quantity`` fields. In JSON
   these fields would look like:
   
   .. code-block:: javascript
   
      {"name": "notebook", "qty": 50}
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Start Thinking in JSON
   ``````````````````````````````

   
   While a table might seem like a good place to store data, as you can
   see from the example above, there are fields in this data set that
   require multiple values and would not be easy to search or display if
   modeled in a single column (for example -- ``size`` and ``tags``).
   
   In a SQL database you might solve this problem by creating a
   relational table.
   
   In MongoDB, data is stored as documents. These documents are stored in
   MongoDB in ``JSON`` (JavaScript Object Notation) format. JSON documents support
   embedded fields, so related data and lists of data can be stored with
   the document instead of an external table.
   
   JSON is formatted as name/value pairs. In JSON documents, fieldnames
   and values are separated by a colon, fieldname and value pairs are
   separated by commas, and sets of fields are encapsulated in "curly
   braces" ({}).
   
   If you wanted to begin to model one of the rows above, for example
   this one:
   
   .. list-table::
      :header-rows: 1
      :widths: auto
      :class: guide-tablenate-odd
   
      * - name
        - quantity
        - size
        - status
        - tags
        - rating
   
      * - notebook
        - 50
        - 8.5x11,in
        - A
        - college-ruled,perforated
        - 8
   
   You might start with the ``name`` and ``quantity`` fields. In JSON
   these fields would look like:
   
   .. code-block:: javascript
   
      {"name": "notebook", "qty": 50}
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Identify Candidates for Embedded Data and Model Your Data
   `````````````````````````````````````````````````````````

   
   Next you will decide which fields require multiple values. These
   fields will be candidates for embedded documents or lists/arrays of
   embedded documents within the document.
   
   For example, in the data above, ``size`` might consist of three
   fields:
   
   .. code-block:: javascript
   
      { "h": 11, "w": 8.5, "uom": "in" }
   
   And some items have multiple ratings, so ``ratings`` might be
   represented as a list of documents containing the field ``scores``:
   
   .. code-block:: javascript
   
      [ { "score": 8 }, { "score": 9 } ]
   
   And you might need to handle multiple tags per item. So you might
   store them in a list too.
   
   .. code-block:: javascript
   
      [ "college-ruled", "perforated" ]
   
   Finally, a JSON document that stores an inventory item might look like this:
   
   .. code-block:: javascript
   
   
      {
       "name": "notebook",
       "qty": 50,
       "rating": [ { "score": 8 }, { "score": 9 } ],
       "size": { "height": 11, "width": 8.5, "unit": "in" },
       "status": "A",
       "tags": [ "college-ruled", "perforated"]
      }
   
   This looks very different from the tabular data  structure you started
   with in Step 1.
   
   .. note::
   
      It's a JSON standard to quote field names.
   
   
   
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Identify Candidates for Embedded Data and Model Your Data
   `````````````````````````````````````````````````````````````````

   
   Next you will decide which fields require multiple values. These
   fields will be candidates for embedded documents or lists/arrays of
   embedded documents within the document.
   
   For example, in the data above, ``size`` might consist of three
   fields:
   
   .. code-block:: javascript
   
      { "h": 11, "w": 8.5, "uom": "in" }
   
   And some items have multiple ratings, so ``ratings`` might be
   represented as a list of documents containing the field ``scores``:
   
   .. code-block:: javascript
   
      [ { "score": 8 }, { "score": 9 } ]
   
   And you might need to handle multiple tags per item. So you might
   store them in a list too.
   
   .. code-block:: javascript
   
      [ "college-ruled", "perforated" ]
   
   Finally, a JSON document that stores an inventory item might look like this:
   
   .. code-block:: javascript
   
   
      {
       "name": "notebook",
       "qty": 50,
       "rating": [ { "score": 8 }, { "score": 9 } ],
       "size": { "height": 11, "width": 8.5, "unit": "in" },
       "status": "A",
       "tags": [ "college-ruled", "perforated"]
      }
   
   This looks very different from the tabular data  structure you started
   with in Step 1.
   
   .. note::
   
      It's a JSON standard to quote field names.
   
   
   
   

