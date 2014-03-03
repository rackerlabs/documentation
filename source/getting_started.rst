Getting Started Guide
=====================

ObjectRocket provides a signup wizard to help you with the initial ObjectRocket set up process. This Getting Started Guide
provides an overview of the concepts and processes involved in the initial set up, so you can begin using your ObjectRocket
instances quickly.


Set up requirements
~~~~~~~~~~~~~~~~~~~~~~
You need the following resources to use the ObjectRocket service:

- An ObjectRocket account 
- Credit card information for billing
- Subscription to an ObjectRocket plan
- An ObjectRocket instance.
- A MongoDB database hosted on the ObjectRocket instance.
- A network ACL to provide outside network access to the ObjectRocket system.

 .. _shard: http://docs.mongodb.org/manual/core/sharded-cluster-shards/
 
 
Before you begin
~~~~~~~~~~~~~~~~~~~~~~ 
 
Review the following information to learn about the concepts and processes relevant to the setup process.
Understanding this information will help you provide the correct information during the sign up, set up, and 
configuration process.
 
'ObjectRocket plan'_
'ObjectRocket instance'_
'MongoDB database setup'_
'Network ACL'_


ObjectRocket plan
------------------
An ObjectRocket plan is the same as a single 'shard'_. The plan specifies the unit of MongoDB storage required. 
ObjectRocket offers a variety of plans and pricing options. Before you begin the sign up process, 
 review the 'plan descirptions' to determine which one meets your requirements. You can always upgrade your plan as your
 
 
.. WRITER QUESTION:  In your current Getting Started, you say that plan and a single shard are synonyms, but then the descritption
says that you can add always add more shards to your plan as your data set grows.  That's a little confusing.  Also.  what is a "unit".

 
 .. _plan descriptions: http://www.objectrocket.com/pricing
 
Instance
------------------
An instance is a complete MongoDB cluster that provides the container for interacting with the ObjectRocket service.
Instances can be hosted in Rackspacee zones or AWS Direct Connect zones. When you create an instance, ObjectRocket creates
the connect string required to establish the database connection.


MongoDB database setup
----------------------
After you create an instance, you can add one or more MongoDB databases to that instance. You can create a new database, or 
copy an existing database from a remote system. During the initial set up process, specify a database name, and at least one username and
password.  You can add more users later. 


Network ACL
------------------
You need an order to access the ObjectRocket system from an outside network, you must create a network ACL. The ACL is based 
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


Sign up with ObjectRocket
-------------------------
Use the ObjectRocket signup wizard to set up the account, specify billing information, select a service plan, and
create your first instance. Then, you can add databases and create and configure the ACL.

.. _signup wizard: https://app.objectrocket.com/sign_up1

After you complete the initial set up, use the following links to manage your account, billing information, and ObjectRocket instance.

- 'Accounts'
- 'Billing'
- 'Instance'

.. _Accounts: https://app.objectrocket.com/accounts
.. _Billing:  https://app.objectrocket.com/billing
.. _Instance: https://app.objectrocket.com/instances


When the database set up is complete, you are ready to use your ObjectRocket instance. You can find the database connect 
string on the ObjectRocket Instances page.

..WRITER COMMNENT 

You are all set to start using your ObjectRocket instance.  Your connect string details are listed on the instances page.

If you have any questions, concerns or comments. contact ObjectRocket Support'.  please reach out at support@objectrocket.com.
