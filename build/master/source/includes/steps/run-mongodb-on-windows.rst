.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Set up the MongoDB environment.
   ```````````````````````````````

   MongoDB requires a :term:`data directory <dbpath>` to store all
   data. MongoDB's default data directory path is the absolute path
   ``\data\db`` on the drive from which you start MongoDB. Create
   this folder by running the following command in a
   :guilabel:`Command Prompt`:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      md \data\db
      

   You can specify an alternate path for data files using the
   :option:`--dbpath <mongod.--dbpath>` option to
   :binary:`~bin.mongod.exe`, for example:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath d:\test\mongodb\data
      

   If your path includes spaces, enclose the entire path in double
   quotes, for example:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath "d:\test\mongo db data"
      

   You may also specify the ``dbpath`` in a :manual:`configuration file
   </reference/configuration-options>`.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Set up the MongoDB environment.
   ```````````````````````````````````````

   MongoDB requires a :term:`data directory <dbpath>` to store all
   data. MongoDB's default data directory path is the absolute path
   ``\data\db`` on the drive from which you start MongoDB. Create
   this folder by running the following command in a
   :guilabel:`Command Prompt`:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      md \data\db
      

   You can specify an alternate path for data files using the
   :option:`--dbpath <mongod.--dbpath>` option to
   :binary:`~bin.mongod.exe`, for example:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath d:\test\mongodb\data
      

   If your path includes spaces, enclose the entire path in double
   quotes, for example:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath "d:\test\mongo db data"
      

   You may also specify the ``dbpath`` in a :manual:`configuration file
   </reference/configuration-options>`.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Start MongoDB.
   ``````````````

   To start MongoDB, run :binary:`~bin.mongod.exe`. For example, from the
   :guilabel:`Command Prompt`:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe"
      

   This starts the main MongoDB database process. The ``waiting for
   connections`` message in the console output indicates that the
   :binary:`~bin.mongod.exe` process is running successfully.
   
   Depending on the security level of your system, Windows may pop up a
   :guilabel:`Security Alert` dialog box about blocking "some features" of
   ``C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe`` from communicating
   on networks. All users should select ``Private Networks, such as my home or
   work network`` and click ``Allow access``. For additional information on
   security and MongoDB, please see the :manual:`Security Documentation </security>`.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Start MongoDB.
   ``````````````````````

   To start MongoDB, run :binary:`~bin.mongod.exe`. For example, from the
   :guilabel:`Command Prompt`:
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe"
      

   This starts the main MongoDB database process. The ``waiting for
   connections`` message in the console output indicates that the
   :binary:`~bin.mongod.exe` process is running successfully.
   
   Depending on the security level of your system, Windows may pop up a
   :guilabel:`Security Alert` dialog box about blocking "some features" of
   ``C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe`` from communicating
   on networks. All users should select ``Private Networks, such as my home or
   work network`` and click ``Allow access``. For additional information on
   security and MongoDB, please see the :manual:`Security Documentation </security>`.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

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

   Step 3: Verify that MongoDB has started successfully
   ````````````````````````````````````````````````````

   Verify that MongoDB has started successfully by
   checking the process output for the following line:
   

   .. code-block:: none
   
      [initandlisten] waiting for connections on port 27017
      

   
   The output should be visible in the terminal or shell window.
   
   You may see non-critical warnings in the process
   output. As long as you see the log line shown above, you can safely
   ignore these warnings during your initial evaluation of MongoDB.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Connect to MongoDB.
   ```````````````````

   To connect to MongoDB through the :binary:`~bin.mongo.exe <mongo>` shell,
   open another :guilabel:`Command Prompt`.
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"
      

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Connect to MongoDB.
   ```````````````````````````

   To connect to MongoDB through the :binary:`~bin.mongo.exe <mongo>` shell,
   open another :guilabel:`Command Prompt`.
   

   .. cssclass:: copyable-code

   .. code-block:: powershell
   
      "C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"
      

