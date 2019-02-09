.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">1</div></div>

   Download the React sample app.
   ``````````````````````````````

   Download the sample app from `github <https://github.com/skerschb/testauth>`_ or clone the repo.
   
   To clone the repo:
   
   .. code-block:: sh
   
      git clone git@github.com:skerschb/testauth.git
   
   Look in the ``src`` folder. In the ``index.js`` toward the top of the file you will see an import
   statement that shows the Stitch package you will need to install to run this application.
   
   .. literalinclude:: /driver-examples/react_stitch_google.js
      :language: javascript
      :dedent: 2
      :start-after: start stitch import
      :end-before: end stitch import
   
   Run ``npm install`` to install the module required.
   
   .. code-block:: sh
   
      npm install mongodb-stitch-browser-sdk
   
   In ``index.js`` you will also see a method called ``setupStitch()``.
   This method is where the stitch client is initialized or assigned,
   and then checked for auth.
   
   .. literalinclude:: /driver-examples/react_stitch_google.js
      :language: javascript
      :dedent: 4
      :start-after: start stitch setup
      :end-before: end stitch setup
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 1: Download the React sample app.
   ``````````````````````````````````````

   Download the sample app from `github <https://github.com/skerschb/testauth>`_ or clone the repo.
   
   To clone the repo:
   
   .. code-block:: sh
   
      git clone git@github.com:skerschb/testauth.git
   
   Look in the ``src`` folder. In the ``index.js`` toward the top of the file you will see an import
   statement that shows the Stitch package you will need to install to run this application.
   
   .. literalinclude:: /driver-examples/react_stitch_google.js
      :language: javascript
      :dedent: 2
      :start-after: start stitch import
      :end-before: end stitch import
   
   Run ``npm install`` to install the module required.
   
   .. code-block:: sh
   
      npm install mongodb-stitch-browser-sdk
   
   In ``index.js`` you will also see a method called ``setupStitch()``.
   This method is where the stitch client is initialized or assigned,
   and then checked for auth.
   
   .. literalinclude:: /driver-examples/react_stitch_google.js
      :language: javascript
      :dedent: 4
      :start-after: start stitch setup
      :end-before: end stitch setup
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">2</div></div>

   Build the sample app.
   `````````````````````

   Once you have downloaded or cloned the app, use ``npm`` to install
   any remaining dependencies (the Stitch dependency has already been
   installed as part of Step 1).
   
   .. code-block:: sh
   
      npm install
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 2: Build the sample app.
   `````````````````````````````

   Once you have downloaded or cloned the app, use ``npm`` to install
   any remaining dependencies (the Stitch dependency has already been
   installed as part of Step 1).
   
   .. code-block:: sh
   
      npm install
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Modify the package.json.
   ````````````````````````

   ``npm`` will install dependencies in the ``node_modules`` directory.
   
   After the packages are installed, there are a few parameters in the
   package.json you will need to modify in order to deploy the application,
   in particular the ``deploy`` and ``homepage`` attributes.
   
   Consult the instructions for your deployment environment for the correct
   parameters to add to your package.json. The package.json that is included
   in the sample app uses `Github Pages <https://pages.github.com/>`_ .
   
   Once you have modified your parameters, it's time to deploy your application.
   
   .. code-block:: sh
   
      npm run deploy
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Modify the package.json.
   ````````````````````````````````

   ``npm`` will install dependencies in the ``node_modules`` directory.
   
   After the packages are installed, there are a few parameters in the
   package.json you will need to modify in order to deploy the application,
   in particular the ``deploy`` and ``homepage`` attributes.
   
   Consult the instructions for your deployment environment for the correct
   parameters to add to your package.json. The package.json that is included
   in the sample app uses `Github Pages <https://pages.github.com/>`_ .
   
   Once you have modified your parameters, it's time to deploy your application.
   
   .. code-block:: sh
   
      npm run deploy
   

.. only:: html or dirhtml or singlehtml

   .. raw:: html
   
      <div class="sequence-block"><div class="bullet-block"><div class="sequence-step">3</div></div>

   Check your results
   ``````````````````

   Once you have deployed your application, check the url for which you have set up
   Google OAuth. You should be directed to a google login page. Once you authenticate,
   the application will render your username on the page.
   

   .. raw:: html
   
      </div>

.. only:: not(html or dirhtml or singlehtml)

   Step 3: Check your results
   ``````````````````````````

   Once you have deployed your application, check the url for which you have set up
   Google OAuth. You should be directed to a google login page. Once you authenticate,
   the application will render your username on the page.
   

