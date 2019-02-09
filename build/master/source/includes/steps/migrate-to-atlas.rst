.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Launch your target replica set in MongoDB Atlas.
   ````````````````````````````````````````````````

   
   See :doc:`Create an Atlas Account and Cluster </cloud/atlas>`
   for instructions.
   
   .. note::
   
      Your target cluster must use ``M10`` or larger instance nodes.
      For development or staging environments, deploy a cluster
      with ``M10`` or ``M20`` instance nodes. For production workloads,
      select ``M30`` or larger instance nodes.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Launch your target replica set in MongoDB Atlas.
   ````````````````````````````````````````````````````````

   
   See :doc:`Create an Atlas Account and Cluster </cloud/atlas>`
   for instructions.
   
   .. note::
   
      Your target cluster must use ``M10`` or larger instance nodes.
      For development or staging environments, deploy a cluster
      with ``M10`` or ``M20`` instance nodes. For production workloads,
      select ``M30`` or larger instance nodes.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Open Atlas Live Migration Service.
   ``````````````````````````````````

   
   On the Overview page of your new target cluster, click the ellipsis
   (...) button and select :guilabel:`Migrate Data to this Cluster`.
   
   .. figure:: /images/atlas-deployment.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Open Atlas Live Migration Service.
   ``````````````````````````````````````````

   
   On the Overview page of your new target cluster, click the ellipsis
   (...) button and select :guilabel:`Migrate Data to this Cluster`.
   
   .. figure:: /images/atlas-deployment.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Click :guilabel:`I'm ready to migrate`.
   ```````````````````````````````````````

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Click :guilabel:`I'm ready to migrate`.
   ```````````````````````````````````````````````

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Whitelist the Atlas Live Migration Service on your AWS source cluster.
   ``````````````````````````````````````````````````````````````````````

   
   At the top of the :guilabel:`Migrate Data to Cluster` modal, Atlas displays
   the IP address ranges that must be accessible from your source cluster.
   The address ranges displayed depend on the location of your target
   cluster and can change, so verify that you enter the address ranges
   as displayed in the modal.
   
   AWS EC2 servers are protected from unauthorized network access using
   `Security Groups <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules-reference.html>`_.
   To whitelist new IP address ranges, either create a new Security Group, or
   modify your existing Security Group to permit inbound network access
   from the displayed IP address ranges.
   
   Here is an example security group that grants access to Atlas Live Migration Service.
   
   .. figure:: /images/aws-inbound-rules.png
      :figwidth: 760
   
   If you create a new Security Group, you must associate it with
   the EC2 instances running your source cluster. In the AWS EC2 console,
   click the :guilabel:`Actions` dropdown and select :guilabel:`Change
   Security Group`.
   
   .. figure:: /images/aws-change-security-group.gif
      :figwidth: 760
   
   For additional information on creating or modifying Security Groups, see `Adding Rules to a Security Group
   <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html#adding-security-group-rule>`_
   in the AWS EC2 documentation.
   
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Whitelist the Atlas Live Migration Service on your AWS source cluster.
   ``````````````````````````````````````````````````````````````````````````````

   
   At the top of the :guilabel:`Migrate Data to Cluster` modal, Atlas displays
   the IP address ranges that must be accessible from your source cluster.
   The address ranges displayed depend on the location of your target
   cluster and can change, so verify that you enter the address ranges
   as displayed in the modal.
   
   AWS EC2 servers are protected from unauthorized network access using
   `Security Groups <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules-reference.html>`_.
   To whitelist new IP address ranges, either create a new Security Group, or
   modify your existing Security Group to permit inbound network access
   from the displayed IP address ranges.
   
   Here is an example security group that grants access to Atlas Live Migration Service.
   
   .. figure:: /images/aws-inbound-rules.png
      :figwidth: 760
   
   If you create a new Security Group, you must associate it with
   the EC2 instances running your source cluster. In the AWS EC2 console,
   click the :guilabel:`Actions` dropdown and select :guilabel:`Change
   Security Group`.
   
   .. figure:: /images/aws-change-security-group.gif
      :figwidth: 760
   
   For additional information on creating or modifying Security Groups, see `Adding Rules to a Security Group
   <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html#adding-security-group-rule>`_
   in the AWS EC2 documentation.
   
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Validate your AWS credentials with Atlas Live Migration Service.
   ````````````````````````````````````````````````````````````````

   
   a. On the :guilabel:`Migrate Data to Cluster` modal, enter the hostname
      and port number of the primary node in your source AWS source cluster
      that Atlas will use to perform the data migration.
   
      .. note::
   
         The address must be resolvable over the public internet, so do not use
         the private IP address of the node.
   
   #. Enter the MongoDB username and password from the AWS source cluster
      in :guilabel:`Username/Password`.
   
   #. If SSL is enabled on the source cluster, toggle the :guilabel:`Is SSL enabled`
      to :guilabel:`Yes` and upload the CA file that your source AWS cluster
      uses.
   
   #. Click :guilabel:`Validate`.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Validate your AWS credentials with Atlas Live Migration Service.
   ````````````````````````````````````````````````````````````````````````

   
   a. On the :guilabel:`Migrate Data to Cluster` modal, enter the hostname
      and port number of the primary node in your source AWS source cluster
      that Atlas will use to perform the data migration.
   
      .. note::
   
         The address must be resolvable over the public internet, so do not use
         the private IP address of the node.
   
   #. Enter the MongoDB username and password from the AWS source cluster
      in :guilabel:`Username/Password`.
   
   #. If SSL is enabled on the source cluster, toggle the :guilabel:`Is SSL enabled`
      to :guilabel:`Yes` and upload the CA file that your source AWS cluster
      uses.
   
   #. Click :guilabel:`Validate`.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">6</div></div>

   Click :guilabel:`Start Migration`.
   ``````````````````````````````````

   
   A countdown timer in a progress bar indicates how much time remains
   before your target cluster is ready to migrate data from your source
   cluster. Wait until the countdown timer and the :guilabel:`Start Cutover`
   button are green before proceeding to the next step.
   
   .. figure:: /images/migration-complete.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 6: Click :guilabel:`Start Migration`.
   ``````````````````````````````````````````

   
   A countdown timer in a progress bar indicates how much time remains
   before your target cluster is ready to migrate data from your source
   cluster. Wait until the countdown timer and the :guilabel:`Start Cutover`
   button are green before proceeding to the next step.
   
   .. figure:: /images/migration-complete.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">7</div></div>

   Click :guilabel:`Start Cutover`.
   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   
   Your AWS cluster and your Atlas cluster are now in sync. Atlas will maintain
   this synchronized state for 72 hours. If you need more time, syncing can be
   extended for another 24 hours.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 7: Click :guilabel:`Start Cutover`.
   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   
   Your AWS cluster and your Atlas cluster are now in sync. Atlas will maintain
   this synchronized state for 72 hours. If you need more time, syncing can be
   extended for another 24 hours.
   

