# blockchain-property-registraion-project-by-Ayush
blockchain property registration project 
Property Registration is a project that aims at registering property/ land and preventing frauds of the same. It is a mere record of sales transaction using Blockchain technology developed using Hyperledger Composer.

Overview of the Network:-

Participants: Buyer, Seller, Registrar
Assets: Property, PropertyListing
PropertyListing will contain only property which are for sale
Transactions: Created, IntentForSale, Registered
In transaction Created we are changing the status of the property if IntentForSale is checked and if Public is also checked, the asset value is added to the PropertyListing asset.

In transaction IntentForSale,Property which is for sale and are checked as Private are taken from Property asset and Sales transaction is done.

Property which are for sale and are checked as Public are taken from PropertyListing asset and Sales transaction is done. After the transaction takes place, there is a change in Buyer and Sellers Balance, Property Owner and the Status from IntentForSale to Registered

In transaction Registered, the property value whose Status is Registered are added to the Property asset and removed from PropertyListing asset.

To test this Business Network Definition in the Test tab:
In the Buyer participant registry, create a new participant.



In the Registrar participant registry, create a new participant.



In the Seller participant registry, create two participants.





In the Property asset registry, create two assets of a property identified by PID.

In first asset, the property will be for "IntentForSale" and "Public".


In Second asset, the property will be for "IntentForSale" and "Private".


In the PropertyListing asset registry, create a property listing for property PLID:1.

Property which are for "ForSale" can only be there under PropertyListing asset.


As soon as Property asset has been created, participant can submit “Created” transactions, the status of properties checked for “IntentForSale” will get changed to “IntentForSale” and the properties which are checked for “IntentForSale” and are “Public” are added to “PropertyListing” asset for sale. We are checking for two properties under “Property” asset.

1. Property which is for “IntentForSale” and is “Public”.


2. Property which is for “IntentForSale” and is “Private”. Therefore, only status for this property will change and it will not be added in “PropertyListing” asset.


In “Created” Transaction, we have taken PID= “2” as Property asset or PropertyListing asset may have different unique ID, therefore, we are taking PID which is unique. To make a sale agreement between Buyer and Seller, “IntentForSale” transaction is submitted. Here we have two cases:- 1. Property which are “IntentForSale” and are “Private” can be sold only from “Property” asset. Therefore, we will make a contract for these properties individually.


2. Property which are “IntentForSale” and are “Public” can be sold only from “PropertyListing” asset. Therefore, we will make a contract for these properties individually.


After “IntentForSale” transaction has been completed, the status changes to “Registered”.

In “Registered” transaction, the Properties under “PropertyListing” asset and have status “Registered” are added under “Property” asset and removed from “PropertyListing” asset.



Congratulations!
The sales transaction has been done between Buyer and seller, now the Property owner has been changed, Buyer and Seller balance has been updated.

License
Hyperledger Project source code files are made available under the Apache License, Version 2.0 (Apache-2.0), located in the LICENSE file. Hyperledger Project documentation files are made available under the Creative Commons Attribution 4.0 International License (CC-BY-4.0), available at http://creativecommons.org/licenses/by/4.0/.

Click on the image and check the demo video
IMAGE ALT TEXT
