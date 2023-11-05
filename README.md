# Trading System (Market)

The Trading System, or Market, is a platform that facilitates commerce between sellers and buyers. The system consists of a collection of stores, each containing seller information and product inventories. Each product within a store has unique attributes. Users of the system visit the market for purchasing, selling, and management purposes. Users assume various roles within the system, including Sellers, Buyers, and Administrators. A user can take on multiple roles simultaneously.

## User Roles:
- **Seller**: Sellers can open a store and become the store's owner. Store owners are allowed to define purchasing policies (comprising various buying options and associated rules) and discount policies (including different types of discounts and rules for applying them). Additionally, store owners can manage their product inventory and appoint other store owners or managers for their store, with the ability to specify the level of management authority granted.

- **Buyer**: Buyers can access information about stores and the products within them. They can search for products based on various criteria. The product information includes details about the purchase policy and discount policy applied to the products. Users can also register with the system, becoming subscribers, while unregistered users are treated as guests.

- **Administrator**: System administrators handle inquiries from buyers and sellers, ensuring fair and legal trading within the system. They monitor the system's operations and address any issues that may arise.

## Key Features:
- Access store and product information.
- Search for products based on specific criteria.
- Register as a system subscriber.
- Real-time notifications.
- Integration with external services for specific operations, such as payment processing and product delivery.

## Security and Usability:
The system adheres to various security and usability requirements to protect user information and provide a seamless user experience.

## Project Development

The development of the Trading System consists of four versions, including a preliminary version (Version 0), which focuses on modeling the system's domain layer. The development approach is characterized by short development cycles and follows an Agile development methodology, incorporating aspects of Model-Based Software Engineering (MBSE).

Each version of the system is based on a general requirements document, which serves as the initial specification for the system. This document encapsulates the core essence of the system and aids in decision-making during the development process. However, subsequent versions expand upon and may even alter certain parts of the initial specification, in a way that does not contradict the fundamental description of the system.

Changes in the project's scope and specifications can result from errors in the initial specification, customer requirements, or other modifications requested during the development process. Each version builds upon its predecessors and includes new features, as well as changes to meet evolving requirements.

## Configuration

1. Open the `config.properties` file located in the `src/main/resources` directory of the project.

2. Update the database configuration with the provided credentials:

   ```properties
   dbType = 'postgresql';
   host = '139.59.209.55';
   port = 5432;
   db = 'dev_db'; 
   user = 'postgres';
   password = '123';
dbType: Specifies the type of the database. In this case, it is set to 'postgresql', indicating that the system is using PostgreSQL as the database.
host: Represents the IP address or hostname of the database server. The provided value is '139.59.209.55', which is the specific address where the database is hosted.
port: Specifies the port number on which the database server is listening. The provided value is 5432, which is the default port for PostgreSQL.
db: Indicates the name of the database to be used. In this case, the value is 'dev_db', representing the specific database that the system will connect to.
user: Specifies the username for connecting to the database. The provided value is 'postgres', which is the username associated with the PostgreSQL database.
password: Represents the password for the specified database user. The provided value is '123', which is the password associated with the PostgreSQL user.
Mode (Optional): This field allows for specifying the mode of operation for the system. It can have three possible values:

create: This mode is used when you want to reset the database during system startup. It will drop the existing tables and recreate them from scratch.
update: This mode is used when you want to continue using the existing database without making any changes to the data.
create-delete: This mode is used when you want to reset the database during system startup and also delete all data when the system is shut down. It combines the functionality of both create and delete operations.
To use the desired mode, you can add the mode field to the config.properties file and set its value accordingly based on your requirements.

Update the following properties with the provided values:

properties
Copy code
scenarioNumber = 3
serviceURL = https://php-server-try.000webhostapp.com/
scenarioNumber: This property represents the specific scenario or data flow to be executed by the system. In this case, the value is set to 3. You can change this to 1/2/3, depending on your requirements. The scenario number determines the sequence of actions, data transformations, or specific functionalities that will be triggered within the system.

serviceURL: The serviceURL property specifies the URL of the external service that the system will interact with. In this case, the value is set to https://php-server-try.000webhostapp.com/.

Save the changes to the config.properties file.

These instructions provide details on how to configure and run the project, including database settings and scenarios for execution. Make sure to follow these steps for setting up and operating the project as needed.
