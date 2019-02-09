.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Create the data directory
   `````````````````````````

   Before you start MongoDB for the first time, create the directory to
   which the :binary:`~bin.mongod` process will write data. By default, the
   :binary:`~bin.mongod` process uses the ``/data/db`` directory. If you create
   a directory other than this one, you must specify that directory in the
   :setting:`dbpath` option when starting the :binary:`~bin.mongod` process
   later in this procedure.
   

   The following example command creates the default ``/data/db`` directory:
   

   .. code-block:: sh
   
      mkdir -p /data/db
      

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Create the data directory
   `````````````````````````````````

   Before you start MongoDB for the first time, create the directory to
   which the :binary:`~bin.mongod` process will write data. By default, the
   :binary:`~bin.mongod` process uses the ``/data/db`` directory. If you create
   a directory other than this one, you must specify that directory in the
   :setting:`dbpath` option when starting the :binary:`~bin.mongod` process
   later in this procedure.
   

   The following example command creates the default ``/data/db`` directory:
   

   .. code-block:: sh
   
      mkdir -p /data/db
      

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Set permissions for the data directory
   ``````````````````````````````````````

   Before running :binary:`~bin.mongod` for the first time, ensure that the
   user account running :binary:`~bin.mongod` has read and write permissions
   for the directory.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Set permissions for the data directory
   ``````````````````````````````````````````````

   Before running :binary:`~bin.mongod` for the first time, ensure that the
   user account running :binary:`~bin.mongod` has read and write permissions
   for the directory.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Run MongoDB
   ```````````

   To run MongoDB, run the :binary:`~bin.mongod` process at the system prompt.
   If necessary, specify the path of the :binary:`~bin.mongod` or the data
   directory. See the following examples.
   

   Run without specifying paths
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If your system ``PATH`` variable includes the location of the
   :binary:`~bin.mongod` binary and if you use the default data directory
   (i.e., ``/data/db``), simply enter ``mongod`` at the system prompt:
   

   .. code-block:: sh
   
      mongod
      

   Specify the path of the :binary:`~bin.mongod`
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If your ``PATH`` does not include the location of the
   :binary:`~bin.mongod` binary, enter the full path to the :binary:`~bin.mongod`
   binary at the system prompt:
   

   .. code-block:: sh
   
      <path to binary>/mongod
      

   Specify the path of the data directory
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If you do not use the default data directory (i.e., ``/data/db``),
   specify the path to the data directory using the
   :option:`--dbpath <mongod.--dbpath>` option:
   

   .. code-block:: sh
   
      mongod --dbpath <path to data directory>
      

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Run MongoDB
   ```````````````````

   To run MongoDB, run the :binary:`~bin.mongod` process at the system prompt.
   If necessary, specify the path of the :binary:`~bin.mongod` or the data
   directory. See the following examples.
   

   Run without specifying paths
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If your system ``PATH`` variable includes the location of the
   :binary:`~bin.mongod` binary and if you use the default data directory
   (i.e., ``/data/db``), simply enter ``mongod`` at the system prompt:
   

   .. code-block:: sh
   
      mongod
      

   Specify the path of the :binary:`~bin.mongod`
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If your ``PATH`` does not include the location of the
   :binary:`~bin.mongod` binary, enter the full path to the :binary:`~bin.mongod`
   binary at the system prompt:
   

   .. code-block:: sh
   
      <path to binary>/mongod
      

   Specify the path of the data directory
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   If you do not use the default data directory (i.e., ``/data/db``),
   specify the path to the data directory using the
   :option:`--dbpath <mongod.--dbpath>` option:
   

   .. code-block:: sh
   
      mongod --dbpath <path to data directory>
      

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Verify that MongoDB has started successfully
   ````````````````````````````````````````````

   Verify that MongoDB has started successfully by
   checking the process output for the following line:
   

   .. code-block:: none
   
      [initandlisten] waiting for connections on port 27017
      

   
   The output should be visible in the terminal or shell window.
   
   You may see non-critical warnings in the process
   output. As long as you see the log line shown above, you can safely
   ignore these warnings during your initial evaluation of MongoDB.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Verify that MongoDB has started successfully
   ````````````````````````````````````````````````````

   Verify that MongoDB has started successfully by
   checking the process output for the following line:
   

   .. code-block:: none
   
      [initandlisten] waiting for connections on port 27017
      

   
   The output should be visible in the terminal or shell window.
   
   You may see non-critical warnings in the process
   output. As long as you see the log line shown above, you can safely
   ignore these warnings during your initial evaluation of MongoDB.
   

