.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Your data is currently in a MongoDB database.
   `````````````````````````````````````````````

   
   This guide focuses on migrating to Atlas from an existing MongoDB deployment
   on AWS. If you have data in other database systems, such as MySQL, PostgreSQL, or
   DynamoDB, please `contact us <https://mongodbcom-node-staging-2.corp.mongodb.com/contact>`_
   for help with your migration.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Your data is currently in a MongoDB database.
   `````````````````````````````````````````````````````

   
   This guide focuses on migrating to Atlas from an existing MongoDB deployment
   on AWS. If you have data in other database systems, such as MySQL, PostgreSQL, or
   DynamoDB, please `contact us <https://mongodbcom-node-staging-2.corp.mongodb.com/contact>`_
   for help with your migration.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Your current MongoDB database is running MongoDB 2.6+
   `````````````````````````````````````````````````````

   
   Atlas supports the latest versions of MongoDB: 3.4, 3.6, and 4.0.
   If you're running MongoDB version 2.6 or greater, the Atlas Live Migration
   Service can move your data directly into a newer database version.
   Update your `MongoDB drivers <https://docs.mongodb.com/ecosystem/drivers>`_
   and make any necessary code changes at the application level to ensure
   compatibility. If you're running a version older than 2.6, see
   `Upgrade MongoDB to 2.6 <https://docs.mongodb.com/v2.6/release-notes/2.6-upgrade/index.html>`_
   for upgrade instructions.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Your current MongoDB database is running MongoDB 2.6+
   `````````````````````````````````````````````````````````````

   
   Atlas supports the latest versions of MongoDB: 3.4, 3.6, and 4.0.
   If you're running MongoDB version 2.6 or greater, the Atlas Live Migration
   Service can move your data directly into a newer database version.
   Update your `MongoDB drivers <https://docs.mongodb.com/ecosystem/drivers>`_
   and make any necessary code changes at the application level to ensure
   compatibility. If you're running a version older than 2.6, see
   `Upgrade MongoDB to 2.6 <https://docs.mongodb.com/v2.6/release-notes/2.6-upgrade/index.html>`_
   for upgrade instructions.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Your current deployment is a MongoDB replica set.
   `````````````````````````````````````````````````

   
   If your deployment is currently a standalone instance, you must first
   :manual:`convert it to a replica set </tutorial/convert-standalone-to-replica-set>`.
   Live migration of data from sharded clusters is not supported.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Your current deployment is a MongoDB replica set.
   `````````````````````````````````````````````````````````

   
   If your deployment is currently a standalone instance, you must first
   :manual:`convert it to a replica set </tutorial/convert-standalone-to-replica-set>`.
   Live migration of data from sharded clusters is not supported.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Authentication is enabled on your source deployment
   ```````````````````````````````````````````````````

   
   The migration process requires that authentication is enabled on your
   source cluster in AWS. See :manual:`Enable Auth </tutorial/enable-authentication>`
   for instructions on enabling authentication.
   
   You can verify that authentication is enabled on your source cluster
   using the :manual:`mongo </reference/program/mongo/>` command:
   
   .. code-block:: sh
   
      mongo <mongodb-connection-string> -u <mongodb-username> -p --authenticationDatabase admin
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Authentication is enabled on your source deployment
   ```````````````````````````````````````````````````````````

   
   The migration process requires that authentication is enabled on your
   source cluster in AWS. See :manual:`Enable Auth </tutorial/enable-authentication>`
   for instructions on enabling authentication.
   
   You can verify that authentication is enabled on your source cluster
   using the :manual:`mongo </reference/program/mongo/>` command:
   
   .. code-block:: sh
   
      mongo <mongodb-connection-string> -u <mongodb-username> -p --authenticationDatabase admin
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   The database user from your source cluster on AWS that you will use to perform the migration has the required MongoDB roles.
   ````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

   
   The user must have the :authrole:`clusterMonitor` and :authrole:`backup` roles. To verify
   that the database user that you intend to use for migration has the appropriate
   roles, run the :manual:`db.getUser() </reference/method/db.getUser>` command.
   
   .. code-block:: sh
   
      testRS:PRIMARY> use admin
      switched to db admin
      testRS:PRIMARY> db.getUser("admin")
      {
        "_id" : "admin.admin",
        "user" : "admin",
        "db" : "admin",
        "roles" : [
          {
            "role" : "backup",
            "db" : "admin"
          },
          {
            "role" : "clusterMonitor",
            "db" : "admin"
          }
        ]
      }
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: The database user from your source cluster on AWS that you will use to perform the migration has the required MongoDB roles.
   ````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

   
   The user must have the :authrole:`clusterMonitor` and :authrole:`backup` roles. To verify
   that the database user that you intend to use for migration has the appropriate
   roles, run the :manual:`db.getUser() </reference/method/db.getUser>` command.
   
   .. code-block:: sh
   
      testRS:PRIMARY> use admin
      switched to db admin
      testRS:PRIMARY> db.getUser("admin")
      {
        "_id" : "admin.admin",
        "user" : "admin",
        "db" : "admin",
        "roles" : [
          {
            "role" : "backup",
            "db" : "admin"
          },
          {
            "role" : "clusterMonitor",
            "db" : "admin"
          }
        ]
      }
   

