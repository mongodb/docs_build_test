.. cssclass:: copyable-code

.. code-block:: bat

   msiexec.exe /l*v mdbinstall.log  /qb /i mongodb-win32-x86_64-2012plus-1.0-signed.msi ^
               ADDLOCAL="Server,ServerService,Client" ^
               SHOULD_INSTALL_COMPASS="0" 

