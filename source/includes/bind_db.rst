.. tabs-drivers::

   tabs:
     - id: shell
       content: |

         To switch to the ``test`` database in the ``mongo`` shell, type

         .. code-block:: sh

            use test

     - id: compass
       content: |

         If the database has not been created already, click the
         :guilabel:`Create Database` button.

         .. figure:: /images/compass-create-database.png
            :alt: Screeenshot after connecting with the "Create Database" button.
            :figwidth: 750px

         Select the ``test`` database on the left side of the Compass
         interface. Compass will list all of the collections in the
         database below the database name.

         .. figure:: /images/compass-select-test-database.png
            :alt: Screenshot of the MongoDB Compass UI showing with the "test" database selected in the list of databases in the cluster.
            :figwidth: 500px

     - id: python
       content: |

         To access the ``test`` database:

         .. code-block:: python

             db = client.test

     - id: motor
       content: |

         To access the ``test`` database:

         .. code-block:: python

            db = client.test


     - id: java-sync
       content: |

         Switch to the ``test`` database and
         access the ``inventory`` collection.

         .. code-block:: java

            MongoDatabase mongoDB = mongoClient.getDatabase("test");
            MongoCollection<Document> collection = mongoDB.getCollection("inventory");

     - id: nodejs
       content: |

         Within the connect block, set ``db`` to the ``test`` database.

         .. code-block:: javascript

            const db = client.db("test");

     - id: csharp
       content: |

         Switch to the ``test`` database and
         access the ``inventory`` collection.

         .. code-block:: csharp

            var database = client.GetDatabase("test");
            var collection = database.GetCollection<BsonDocument>("inventory");

     # - id: php
     #  content: |

     #   .. code-block:: php
     #
     #      $db = $manager->test;


     # - id: perl
     #  content: |

     #    .. code-block:: perl

     #       use MongoDB;
     #       my $client = MongoDB->connect('<URISTRING>');
     #       my $db = $client->get_database('test');


     # - id: ruby
     #   content: |
     #      If you specified `test` as your database in your URI string,
     #      you should already be connected to the `test` database.
     #      You can also use JSON to configure the connect options. Note
     #      that you will need to pass in the authSource along with the
     #      username and password, or as part of the URI String.
     #
     #      .. code-block:: ruby
     #
     #         client_options = {
     #           database: 'test',
     #           user: '<USERNAME>',
     #           password: '<PASSWORD>',
     #         }
     #
     #         client = Mongo::Client.new('mongodb://localhost:27017/?authSource=admin', client_options);
     #
     # - id: scala
     #   content: |
     #
     #      .. code-block:: scala
     #
     #         val database: MongoDatabase = mongoClient.getDatabase("test")
     #
     #