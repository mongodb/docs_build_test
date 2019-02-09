.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Find the ``mongo`` Shell
   ````````````````````````

   
   The ``mongo`` shell is packaged with the MongoDB Server Community and
   Enterprise distributions, and is also available for users of Atlas as
   a client-only download.
   
   MongoDB binaries are located in a directory that starts with
   "mongodb-". You should see a file named ``mongo``, which is the shell
   executable.
   
   If you do not have ``mongo`` shell installed, follow the install
   directions for your environment.
   
   .. include:: /includes/download-shell-tabs.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Find the ``mongo`` Shell
   ````````````````````````````````

   
   The ``mongo`` shell is packaged with the MongoDB Server Community and
   Enterprise distributions, and is also available for users of Atlas as
   a client-only download.
   
   MongoDB binaries are located in a directory that starts with
   "mongodb-". You should see a file named ``mongo``, which is the shell
   executable.
   
   If you do not have ``mongo`` shell installed, follow the install
   directions for your environment.
   
   .. include:: /includes/download-shell-tabs.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Connect to your MongoDB instance
   ````````````````````````````````

   
   .. include:: /includes/mongo-shell-platform-connect-np.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Connect to your MongoDB instance
   ````````````````````````````````````````

   
   .. include:: /includes/mongo-shell-platform-connect-np.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Switch to the `admin` Database
   ``````````````````````````````

   
   .. code-block:: sh
   
      use admin;
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Switch to the `admin` Database
   ``````````````````````````````````````

   
   .. code-block:: sh
   
      use admin;
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Create the user administrator
   `````````````````````````````

   
   .. code-block:: sh
   
      db.createUser(
        {
          user: "myUserAdmin",
          pwd: "abc123",
          roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
        }
      )
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Create the user administrator
   `````````````````````````````````````

   
   .. code-block:: sh
   
      db.createUser(
        {
          user: "myUserAdmin",
          pwd: "abc123",
          roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
        }
      )
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Create a user for reading and writing to your test database
   ```````````````````````````````````````````````````````````

   
   It is a good idea to keep your admin user credentials separate from
   users that will read and write to the databases on a regular basis.
   
   In this step, create a user that you will use throughout the guides
   for reading and writing test data.
   
   .. code-block:: javascript
   
      db.createUser(
        {
          user: "userreadwrite",
          pwd: "abc123",
          roles: [ { role: "readWriteAnyDatabase", db: "admin" } ]
        }
      )
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Create a user for reading and writing to your test database
   ```````````````````````````````````````````````````````````````````

   
   It is a good idea to keep your admin user credentials separate from
   users that will read and write to the databases on a regular basis.
   
   In this step, create a user that you will use throughout the guides
   for reading and writing test data.
   
   .. code-block:: javascript
   
      db.createUser(
        {
          user: "userreadwrite",
          pwd: "abc123",
          roles: [ { role: "readWriteAnyDatabase", db: "admin" } ]
        }
      )
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">6</div></div>

   Check whether your users have been added
   ````````````````````````````````````````

   
   Run ``show users`` to see if your users were created.
   
   .. code-block:: javascript
   
      show users
   
   You should see output similar to the following:
   
   .. code-block:: sh
   
      {
        "_id" : "admin.myUserAdmin",
        "user" : "myUserAdmin",
        "db" : "admin",
        "roles" : [
          {
            "role" : "userAdminAnyDatabase",
            "db" : "admin"
          }
        ],
        "mechanisms" : [
          "SCRAM-SHA-1",
          "SCRAM-SHA-256"
        ]
      }
      {
        "_id" : "admin.userreadwrite",
        "user" : "userreadwrite",
        "db" : "admin",
        "roles" : [
          {
            "role" : "readWriteAnyDatabase",
            "db" : "admin"
          }
        ],
        "mechanisms" : [
          "SCRAM-SHA-1",
          "SCRAM-SHA-256"
        ]
      }
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 6: Check whether your users have been added
   ````````````````````````````````````````````````

   
   Run ``show users`` to see if your users were created.
   
   .. code-block:: javascript
   
      show users
   
   You should see output similar to the following:
   
   .. code-block:: sh
   
      {
        "_id" : "admin.myUserAdmin",
        "user" : "myUserAdmin",
        "db" : "admin",
        "roles" : [
          {
            "role" : "userAdminAnyDatabase",
            "db" : "admin"
          }
        ],
        "mechanisms" : [
          "SCRAM-SHA-1",
          "SCRAM-SHA-256"
        ]
      }
      {
        "_id" : "admin.userreadwrite",
        "user" : "userreadwrite",
        "db" : "admin",
        "roles" : [
          {
            "role" : "readWriteAnyDatabase",
            "db" : "admin"
          }
        ],
        "mechanisms" : [
          "SCRAM-SHA-1",
          "SCRAM-SHA-256"
        ]
      }
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">7</div></div>

   Exit the ``mongo`` shell
   ````````````````````````

   
   Use ``Ctrl-C`` to exit the ``mongo`` shell.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 7: Exit the ``mongo`` shell
   ````````````````````````````````

   
   Use ``Ctrl-C`` to exit the ``mongo`` shell.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">8</div></div>

   Re-start your MongoDB instance with access control enabled
   ``````````````````````````````````````````````````````````

   
   .. include:: /includes/start-server-auth.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 8: Re-start your MongoDB instance with access control enabled
   ``````````````````````````````````````````````````````````````````

   
   .. include:: /includes/start-server-auth.rst
   

