.. cssclass:: copyable-code

.. code-block:: bat

   msiexec.exe /l*v mdbinstall.log  /qb /i mongodb-win32-x86_64-2012plus-1.0-signed.msi ^
               INSTALLLOCATION="C:\MongoDB\Server\{+version+}\"

