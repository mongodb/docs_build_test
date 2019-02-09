.. cssclass:: copyable-code

.. code-block:: bat

   msiexec.exe /l*v mdbinstall.log  /qb /i mongodb-win32-x86_64-enterprise-windows-64-1.0-signed.msi ^
               SHOULD_INSTALL_COMPASS="0"

