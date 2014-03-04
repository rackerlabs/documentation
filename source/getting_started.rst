Getting Started Guide
=====================

ObjectRocket provides a wizard to guide you through the initial ObjectRocket account setup and service configuration. 
This Getting Started Guide describes the process and concepts relevant to the setup process so you can complete 
the process quickly and start using the ObjectRocket service. 

.. _setup_requirements:

Set up requirements
~~~~~~~~~~~~~~~~~~~~~~
You need the following resources to use the ObjectRocket service:

- An ObjectRocket account 
- Credit card information for billing
- Subscription to an ObjectRocket plan
- An ObjectRocket instance
- A MongoDB database hosted on the ObjectRocket instance.
- A network ACL to provide outside network access to the ObjectRocket system.

.. _before_you_begin_gs:

Before you begin
~~~~~~~~~~~~~~~~~~~~~~ 

Review this section to learn about the concepts and processes relevant to the setup process.

.. _objectrocket_plan_gs:

ObjectRocket plan
------------------
An ObjectRocket plan is the same as a single `shard <http://docs.mongodb.org/manual/core/sharded-cluster-shards/>`_. The plan specifies the unit of MongoDB storage required. 
ObjectRocket offers a variety of plans and pricing options. Before you begin the sign up process, 
review the `plan descriptions <http://www.objectrocket.com/pricing>`_ to decide which one meets your requirements.
You can always upgrade the plan as your data set grows. 
 
 
.. WRITER QUESTION  In your current Getting Started, you say that plan and a single shard are synonyms, but then the descritption
   says that you can add always add more shards to your plan as your data set grows.  That's a little confusing.  Also.  what is a "unit".


.. _objrocket_instance_gs:

ObjectRocket instance
------------------
An instance is a complete MongoDB cluster that provides the container for interacting with the ObjectRocket service.
Instances can be hosted in Rackspacee zones or AWS Direct Connect zones. When you create an instance, ObjectRocket creates
the connect string required to establish the database connection.

.. _mongodb_setup_gs:

MongoDB database setup
----------------------
After you create an instance, you can add one or more MongoDB databases to that instance. You can create a new database, or 
copy an existing database from a remote system. During the initial set up process, specify a database name, and at least one username and
password.  You can add more users later. 

.. _network_acl_gs:

Network ACL
------------------
To grant access to the ObjectRocket system from an outside network, you must create a network ACL. The ACL is based 
on a CIDR type IP address mask and provides access to all databases in an ObjectRocket instances. When you create the ACL, 
you need the IP address of the client system, application server, or web server that will access the ObjectRocket instance.
If you don't know the address, you can detect it using telnet as shown in this example:

.. code-block:: bash

    $>telnet v4address.com
    Trying 184.105.238.114...
    Connected to v4address.com.
    Escape character is '^]'.
    This is the telnet autoresponder at v6address.com.
    You have connected over IPv4.
    Your IP address is 1.1.1.1
    Connection closed by foreign host.
    
If you wanted to provide access to the host in this example, specify 1.1.1.1/32 for the IP address when you are creating the ACL.
After you create the ACL, it might take a few minutes for the ACL to take effect.


.. setup_objrocket_svc_gs:

Set up your ObjectRocket service
~~~~~~~~~~~~~~~~~~~~~~

#. Use the `ObjectRocket signup wizard <https://app.objectrocket.com/sign_up1>`_ to 
   set up your account, specify billing information, select your ObjectRocket plan. amd create your first instance.
#. After the instance is created, add a new database or import a MongoDB database from a remote system. 
   When prompted, enter a database name and the login credentials for the database (username and password).
#. Finally, create a network ACL to allow remote clients and servers to access the ObjectRocket instance.

After adding the database and configuring the network ACL, you can use the database connect 
string on the Instances page to connect to your ObjectRocket service from any client or server included in your ACL list.


.. WRITER COMMENT It would be useful to add a "Test your database connection" section and include an example showing how to connect. 
  Someone at Rackspace wrote this up here:  http://developer.rackspace.com/blog/connect-objectrocket-to-cloud-servers.html.
  Also, are the signup and configuration services available through API calls--maybe only for internal users?  If so,
  we should include an example of how to complete these steps by using API instead of GUI.


Manage your ObjectRocket service
~~~~~~~~~~~~~~~~~~~~~~
After you complete the initial setup process, you can use the following direct links to manage your account, billing information, 
and ObjectRocket instance whenever you are logged into your ObjectRocket account.

- `Accounts <https://app.objectrocket.com/accounts>`_
- `Billing <https://app.objectrocket.com/billing>`_
- `Instance <https://app.objectrocket.com/instances>`_


Contact Support
~~~~~~~~~~~~~~~~~~~~~~

If you have any questions, concerns or comments. contact ObjectRocket Support at support@objectrocket.com.
