.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Create an Atlas deployment
   ``````````````````````````

   If you don't already have an Atlas deployment, :doc:`create one
   </cloud/atlas>` now. You'll need
   a `cluster tier
   <https://docs.atlas.mongodb.com/create-new-cluster/#c-select-the-cluster-tier>`_
   of ``M10`` or larger to perform Live Migration.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Create an Atlas deployment
   ``````````````````````````````````

   If you don't already have an Atlas deployment, :doc:`create one
   </cloud/atlas>` now. You'll need
   a `cluster tier
   <https://docs.atlas.mongodb.com/create-new-cluster/#c-select-the-cluster-tier>`_
   of ``M10`` or larger to perform Live Migration.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Log in to your Compose account
   ``````````````````````````````

   Log in to your `Compose account <https://app.compose.io/session/new>`_
   and navigate to the deployment you want to migrate to Atlas.
   
   .. note::
   
      It will be helpful during the migration process to keep one
      browser window open on your Compose deployment console and one
      window open on your `Atlas console <https://cloud.mongodb.com>`_.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Log in to your Compose account
   ``````````````````````````````````````

   Log in to your `Compose account <https://app.compose.io/session/new>`_
   and navigate to the deployment you want to migrate to Atlas.
   
   .. note::
   
      It will be helpful during the migration process to keep one
      browser window open on your Compose deployment console and one
      window open on your `Atlas console <https://cloud.mongodb.com>`_.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Create an oplog user
   ````````````````````

   To perform the migration process, you need a database user with
   permission to read the oplog on your ``admin`` database. Click the
   :guilabel:`Add-ons` link in the left-side navigation. If you don't
   have the :guilabel:`Oplog Access` add-on, add it with the
   :guilabel:`Add` button.
   
   If you already have the :guilabel:`Oplog Access` add-on, click
   :guilabel:`Configure` to see the oplog user username and password.
   You'll need them both in subsequent migration steps.
   
   .. figure:: /images/compose-oplog-addon.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Create an oplog user
   ````````````````````````````

   To perform the migration process, you need a database user with
   permission to read the oplog on your ``admin`` database. Click the
   :guilabel:`Add-ons` link in the left-side navigation. If you don't
   have the :guilabel:`Oplog Access` add-on, add it with the
   :guilabel:`Add` button.
   
   If you already have the :guilabel:`Oplog Access` add-on, click
   :guilabel:`Configure` to see the oplog user username and password.
   You'll need them both in subsequent migration steps.
   
   .. figure:: /images/compose-oplog-addon.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Begin the Atlas Live Migration process
   ``````````````````````````````````````

   Navigate to your Atlas cluster. Click the ellipsis (:guilabel:`...`)
   button and select :guilabel:`Migrate Data to this Cluster`.
   
   .. figure:: /images/atlas-deployment.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Begin the Atlas Live Migration process
   ``````````````````````````````````````````````

   Navigate to your Atlas cluster. Click the ellipsis (:guilabel:`...`)
   button and select :guilabel:`Migrate Data to this Cluster`.
   
   .. figure:: /images/atlas-deployment.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Review migration steps
   ``````````````````````

   Read through the overview of migration steps in the Live Migration
   dialog window, then click the green :guilabel:`I'm ready to migrate`
   button.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Review migration steps
   ``````````````````````````````

   Read through the overview of migration steps in the Live Migration
   dialog window, then click the green :guilabel:`I'm ready to migrate`
   button.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">6</div></div>

   Add IP address ranges to your Compose deployment whitelist
   ``````````````````````````````````````````````````````````

   For this step you'll need to have browser tabs open
   with both the Atlas Live Migration process dialog from the previous
   step and your Compose deployment dashboard.
   
   On your Compose deployment dashboard, click the :guilabel:`Security`
   link in the left-side navigation. The :guilabel:`Whitelist TCP/HTTP
   IPs` section displays a list of IP address ranges which are allowed
   to access your Compose deployment. Add all four of the IP
   address ranges which are listed at the top of the Atlas Migration
   process dialog window.
   
   .. figure:: /images/compose-add-ips.png
      :figwidth: 700px
   
   .. note::
   
      Your Atlas migration IP address ranges may be different from
      those shown here.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 6: Add IP address ranges to your Compose deployment whitelist
   ``````````````````````````````````````````````````````````````````

   For this step you'll need to have browser tabs open
   with both the Atlas Live Migration process dialog from the previous
   step and your Compose deployment dashboard.
   
   On your Compose deployment dashboard, click the :guilabel:`Security`
   link in the left-side navigation. The :guilabel:`Whitelist TCP/HTTP
   IPs` section displays a list of IP address ranges which are allowed
   to access your Compose deployment. Add all four of the IP
   address ranges which are listed at the top of the Atlas Migration
   process dialog window.
   
   .. figure:: /images/compose-add-ips.png
      :figwidth: 700px
   
   .. note::
   
      Your Atlas migration IP address ranges may be different from
      those shown here.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">7</div></div>

   Add the hostname and port of your Compose deployment to the Atlas Live Migration dialog
   ```````````````````````````````````````````````````````````````````````````````````````

   On the :guilabel:`Oplog Access` add-on page, you'll find a connection
   string with a hostname and port for oplog access. Copy them to the Atlas
   Live Migration dialog.
   
   .. figure:: /images/compose-hostname.png
      :figwidth: 650px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 7: Add the hostname and port of your Compose deployment to the Atlas Live Migration dialog
   ```````````````````````````````````````````````````````````````````````````````````````````````

   On the :guilabel:`Oplog Access` add-on page, you'll find a connection
   string with a hostname and port for oplog access. Copy them to the Atlas
   Live Migration dialog.
   
   .. figure:: /images/compose-hostname.png
      :figwidth: 650px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">8</div></div>

   Enter the oplog user's credentials in the Live Migration dialog
   ```````````````````````````````````````````````````````````````

   Enter the username and password for :guilabel:`oploguser` in the
   Atlas Live Migration dialog window.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 8: Enter the oplog user's credentials in the Live Migration dialog
   ```````````````````````````````````````````````````````````````````````

   Enter the username and password for :guilabel:`oploguser` in the
   Atlas Live Migration dialog window.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">9</div></div>

   Enter your Compose SSL Certificate data
   ```````````````````````````````````````

   If you don't have SSL enabled on your Compose deployment, skip this
   step.
   
   On the :guilabel:`Oplog Access` add-on page, you'll find an SSL
   certificate. Copy it to the CAFile text box on the Atlas Live
   Migration dialog.
   
   .. figure:: /images/compose-cafile.png
      :figwidth: 664px
   
   .. note::
   
      Copy the entire certificate file, including the
      ``BEGIN CERTIFICATE`` and ``END CERTIFICATE`` lines.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 9: Enter your Compose SSL Certificate data
   ```````````````````````````````````````````````

   If you don't have SSL enabled on your Compose deployment, skip this
   step.
   
   On the :guilabel:`Oplog Access` add-on page, you'll find an SSL
   certificate. Copy it to the CAFile text box on the Atlas Live
   Migration dialog.
   
   .. figure:: /images/compose-cafile.png
      :figwidth: 664px
   
   .. note::
   
      Copy the entire certificate file, including the
      ``BEGIN CERTIFICATE`` and ``END CERTIFICATE`` lines.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">10</div></div>

   Validate your Live Migration form
   `````````````````````````````````

   Click the :guilabel:`Validate` button to check that all your form
   fields are valid and your clusters are ready for migration. When your
   form is validated, click the :guilabel:`Start Migration` button.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 10: Validate your Live Migration form
   ``````````````````````````````````````````

   Click the :guilabel:`Validate` button to check that all your form
   fields are valid and your clusters are ready for migration. When your
   form is validated, click the :guilabel:`Start Migration` button.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">11</div></div>

   Start migration
   ```````````````

   When the migration process begins, the Live Migration dialog window
   closes and you are returned to the Atlas cluster overview page. A
   progress bar shows the progess of your migration.
   
   Once the migration is complete, you can begin to update your
   client applications to use the new Atlas connection string.
   
   .. figure:: /images/migration-complete.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 11: Start migration
   ````````````````````````

   When the migration process begins, the Live Migration dialog window
   closes and you are returned to the Atlas cluster overview page. A
   progress bar shows the progess of your migration.
   
   Once the migration is complete, you can begin to update your
   client applications to use the new Atlas connection string.
   
   .. figure:: /images/migration-complete.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">12</div></div>

   Start your cutover
   ``````````````````

   Your Compose deployment and your Atlas cluster are now in sync.
   Atlas will maintain this synchronized state for 72 hours. If you
   need more time, syncing can be extended for another 24 hours.
   
   Click the green :guilabel:`Start cutover` button and follow the
   instructions listed in the dialog window.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 12: Start your cutover
   ```````````````````````````

   Your Compose deployment and your Atlas cluster are now in sync.
   Atlas will maintain this synchronized state for 72 hours. If you
   need more time, syncing can be extended for another 24 hours.
   
   Click the green :guilabel:`Start cutover` button and follow the
   instructions listed in the dialog window.
   

