.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Create or login to an Atlas user account
   ````````````````````````````````````````

   Atlas is MongoDB's cloud-based, database-as-a-service solution.
   In order to use MongoDB in the cloud, you need to create an Atlas user account.
   
   Go to `cloud.mongodb.com
   <https://cloud.mongodb.com?utm_source=atlas-account-guide&utm_campaign=guides&utm_medium=docs>`_
   to create or login to your user account.
   
   If you are creating your user account, as part of the process Atlas
   automatically creates a default "organization" and "project" for you.
   On Atlas, an *organization* correlates to a the name of the
   organization for which the cluster is being created, and the *project*
   is a specific application or initiative that will make use of this MongoDB
   Atlas cluster. You can add additional organizations and
   projects later.
   
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Create or login to an Atlas user account
   ````````````````````````````````````````````````

   Atlas is MongoDB's cloud-based, database-as-a-service solution.
   In order to use MongoDB in the cloud, you need to create an Atlas user account.
   
   Go to `cloud.mongodb.com
   <https://cloud.mongodb.com?utm_source=atlas-account-guide&utm_campaign=guides&utm_medium=docs>`_
   to create or login to your user account.
   
   If you are creating your user account, as part of the process Atlas
   automatically creates a default "organization" and "project" for you.
   On Atlas, an *organization* correlates to a the name of the
   organization for which the cluster is being created, and the *project*
   is a specific application or initiative that will make use of this MongoDB
   Atlas cluster. You can add additional organizations and
   projects later.
   
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Select the Build New Cluster button
   ```````````````````````````````````

   
   If you already had an account when you logged in,
   you will see a ``Clusters`` management panel. A ``cluster`` is a group
   of MongoDB instances that work together to provide high availability
   and fault tolerance.
   
   Select the green ``Build A New Cluster`` button at the center
   of the ``Clusters`` panel.
   
   .. note::
      If you have already built a cluster, you will see this button
      at the right hand side of the panel.
   
   .. figure:: /images/firstcluster.png
      :figwidth: 700px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Select the Build New Cluster button
   ```````````````````````````````````````````

   
   If you already had an account when you logged in,
   you will see a ``Clusters`` management panel. A ``cluster`` is a group
   of MongoDB instances that work together to provide high availability
   and fault tolerance.
   
   Select the green ``Build A New Cluster`` button at the center
   of the ``Clusters`` panel.
   
   .. note::
      If you have already built a cluster, you will see this button
      at the right hand side of the panel.
   
   .. figure:: /images/firstcluster.png
      :figwidth: 700px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Pick your cluster tier
   ``````````````````````

   
   Now it's time to select your cluster tier. In this guide we will be
   setting up a free-tier or ``M0`` cluster.
   
   Ensure that the ``Cloud Provider and Region`` dropdowns have ``Amazon
   Web Services`` and either ``N. Virginia (us-east-1)`` or ``Frankfurt
   (eu-central-1)`` selected.
   
   .. figure:: /images/cloudselect.png
      :figwidth: 700px
   
   Scroll down and click on the ``Cluster Tier`` section. For the free
   tier cluster, select the ``M0`` cluster. You can only create one free
   tier (``M0``) cluster per account. The ``M0`` cluster is not recommended
   for production applications.
   
   .. note::
      The Atlas Live Migration service requires ``M10`` or larger instance
      nodes. For development or staging environments, deploy a cluster
      with ``M10`` or ``M20`` instance nodes. For production workloads, select
      ``M30`` or larger instance nodes.
   
   .. figure:: /images/clusterselect.png
      :figwidth: 837px
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Pick your cluster tier
   ``````````````````````````````

   
   Now it's time to select your cluster tier. In this guide we will be
   setting up a free-tier or ``M0`` cluster.
   
   Ensure that the ``Cloud Provider and Region`` dropdowns have ``Amazon
   Web Services`` and either ``N. Virginia (us-east-1)`` or ``Frankfurt
   (eu-central-1)`` selected.
   
   .. figure:: /images/cloudselect.png
      :figwidth: 700px
   
   Scroll down and click on the ``Cluster Tier`` section. For the free
   tier cluster, select the ``M0`` cluster. You can only create one free
   tier (``M0``) cluster per account. The ``M0`` cluster is not recommended
   for production applications.
   
   .. note::
      The Atlas Live Migration service requires ``M10`` or larger instance
      nodes. For development or staging environments, deploy a cluster
      with ``M10`` or ``M20`` instance nodes. For production workloads, select
      ``M30`` or larger instance nodes.
   
   .. figure:: /images/clusterselect.png
      :figwidth: 837px
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">4</div></div>

   Create your cluster
   ```````````````````

   
   Click the ``Create Cluster`` button at the bottom of the page. If you
   have selected a non free-tier cluster you will be prompted for credit
   card information. It takes a few minutes for the cluster instance to
   spin up.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 4: Create your cluster
   ```````````````````````````

   
   Click the ``Create Cluster`` button at the bottom of the page. If you
   have selected a non free-tier cluster you will be prompted for credit
   card information. It takes a few minutes for the cluster instance to
   spin up.
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">5</div></div>

   Create an administrative username and password
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   
   Atlas prompts you to create an administrative MongoDB user as a part
   of deploying the first Atlas cluster in the project. This user has
   administrative access to any MongoDB cluster you deploy in the Atlas
   project.
   
   Fill in the ``username`` and ``password`` fields. The password should
   be random, long, and complex to ensure system security and to impede
   malicious access.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 5: Create an administrative username and password
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   
   Atlas prompts you to create an administrative MongoDB user as a part
   of deploying the first Atlas cluster in the project. This user has
   administrative access to any MongoDB cluster you deploy in the Atlas
   project.
   
   Fill in the ``username`` and ``password`` fields. The password should
   be random, long, and complex to ensure system security and to impede
   malicious access.
   

