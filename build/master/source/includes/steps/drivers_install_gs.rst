.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Install your client
   ```````````````````

   
   .. include:: /includes/drivers_install.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Install your client
   ```````````````````````````

   
   .. include:: /includes/drivers_install.rst
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Obtain your MongoDB connection string
   `````````````````````````````````````

   
   
   .. include:: /includes/drivers_api_uri.rst
   
   In order to connect to MongoDB, you will need a :ref:`URI string
   <mongodb-uri>`. A ``URI`` (Uniform Resource Identifier) is similar to
   a URL, and is supplied as a parameter to the :binary:`~bin.mongo`
   shell, Compass, and the MongoDB drivers when connecting to a MongoDB
   deployment.
   
   .. include:: /includes/drivers_env_uri.rst
   
   .. important::
   
      If your connection string contains ``$[password]``, you will need
      to replace this string with your password. Use caution
      where you store and enter passwords, particularly when running from
      a shell or command prompt. Special characters in passwords must be
      escaped.
   
   .. uriwriter::
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Obtain your MongoDB connection string
   `````````````````````````````````````````````

   
   
   .. include:: /includes/drivers_api_uri.rst
   
   In order to connect to MongoDB, you will need a :ref:`URI string
   <mongodb-uri>`. A ``URI`` (Uniform Resource Identifier) is similar to
   a URL, and is supplied as a parameter to the :binary:`~bin.mongo`
   shell, Compass, and the MongoDB drivers when connecting to a MongoDB
   deployment.
   
   .. include:: /includes/drivers_env_uri.rst
   
   .. important::
   
      If your connection string contains ``$[password]``, you will need
      to replace this string with your password. Use caution
      where you store and enter passwords, particularly when running from
      a shell or command prompt. Special characters in passwords must be
      escaped.
   
   .. uriwriter::
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Connect to your MongoDB instance
   ````````````````````````````````

   
   .. include:: /includes/drivers_whitelist.rst
   
   .. include:: /includes/drivers_connect.rst
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Connect to your MongoDB instance
   ````````````````````````````````````````

   
   .. include:: /includes/drivers_whitelist.rst
   
   .. include:: /includes/drivers_connect.rst
   

