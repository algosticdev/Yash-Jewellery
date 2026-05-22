
**Introduction**

**Mr. Robert D’costa** started the business from the scratch in 2005. The flagship company of **Yash Gems & Jewelleries (P) ltd** was formed to carry on the business of manufacturing and trading of Gold & Diamond Jewellery. 

•To manufacture diamond Jewellery with ultimate brilliance, ***Yash*** has employed the latest and most advanced technologies for manufacturing diamond jewellery.

•As a supplier to some of the most exclusive retailers, ***Yash*** have intimate knowledge of the cultures and trends of the markets served. The national sales and distribution network team allows them to cultivate a close relationship with the customers and guarantees efficient services. 

•***Yash*** believes in reflecting their jewellery with special magic, conjured by melting of spirit and dedication, labour and craftsmanship, and art of work. The talented designers, skilled craftsmen and dedicated managers use state-of-the-art technology to produce the finest level of diamond jewellery for leading retailers.

•The company’s sincere desire is to give every client a reason to feel good. And policy is to offer top quality merchandise to the customers at the best possible price. 

With a vision and motto of providing its customers products of impeccable quality, ***Yash*** has outnumbered many in innovative design and quality, making itself the benchmark and hallmark of the Indian jewellery industry.







**Proposed Solution**

**To develop a complete web-based solution for *Yash***

•The motive of this Online Jewellery Shopping Web Application is to allow the user to play with the search tool and create different combinatorial search criterion to perform exhaustive search.

•Provide Interactive interface through which a user can interact with different areas of application easily.

•A search engine that provides an easy and convenient way to search for products specific to their needs. The search engine would list a set of products based on the search term and the user can further filter the list based on various parameters.

•Provide Shopping Cart feature thereby allowing the user to add products to or remove products from the shopping cart by dragging the products in to or out of the shopping cart.

•Provides accurate level of security so that transactions can be made confidentially. 

•People who are not much aware of the system can easily make purchase by easy to register interface.












**Requirement Specification:**

- In this system the vendor can launch his/her jewellery products with details of them on website. (Details needs to be captured are as per the table **ItemMst** below in data dictionary section.)
- He can keep these products for sale as well as can update his site with new ornaments time to time. 
- Vendor on his server machine is able to take purchase orders from customers around the world and by validating the truth of orders with verification of customer details he may dispatch the delivery of ornaments to customers via post or courier.
- Vendor can also keep the records of all the customers in a database on his server machine.( **UserRegMst** in data dictionary)
- He also can create reports of his organization sales using database. He can collect bills form customers online using credit card numbers from    customers. 
- On the other hand customers on client machine can access the site for online jewellery shopping from any part of the world using internet service. 
- Customer can select the ornaments from displayed ornaments and can give online orders for purchasing.
- Customer can provide his specific requirement as the weight of diamond, type, brand, carat for gold, name of gems, quality etc.
- Customer can pay his bills using credit card facility for shopping. The valid customers can send gift ornaments to their relatives and friends on other address through this system
- The Search option on the site is very useful for quick search for the ornaments which the customer needs. This reduces the search and browsing time of clients. Ornaments list is available to clients on this system. 
- Customers are able to create their own accounts with individual secured passwords to the vendors. Account holder customer could log in directly by entering login name and password.
- A database should be maintained on the server machine. The database includes customer’s details, login details, product list, order details, Bill details, transaction details etc. the database is helpful in getting quick information reports 
- In addition to the exclusive search for the jewellery, the site should also provide information about diamonds and various gems. Their history as well as benefits of using gems.
- The information about diamond certification should also be provided.
- The home page should be made attractive by posting the various discount schemes/gift offers/ festive offers/new launches etc.

**Data Dictionary**

1. **TABLE NAME: AdminLoginMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|userName|Varchar(50)|Primary key|Administrator Name|
|Password|Varchar(50)|Not Null|Password Of Admin|

1. **TABLE NAME: BrandMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|Brand\_ID|nchar(10)|Primary key|ID Of Particular Brand|
|Brand\_Type|Varchar(50)|Not Null|Type Of Brand (Asmi,D’damas,etc…)|

1. **TABLE NAME: CatMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|Cat\_ID|nchar(10)|Primary key|ID Of Category|
|Cat\_Name|Varchar(50)|Not Null|Name Of Category|

1. **TABLE NAME: CertifyMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|Certify\_ID|nchar(10)|Primary key|ID Of Certification|
|Certify\_Type|Varchar(50)|Not Null|Name Of Certification (918,920,etc…)|

1. **TABLE NAME: DimMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|Style\_Code|Varchar(50)|Foreign Key|Code Of Style|
|DimQlty\_ID|nchar(10)|Foreign Key|ID Of Diamond Quality|
|DimSubType\_ID|nchar(10)|Foreign Key|Sub Type ID Of Diamond|
|Dim\_Crt|Numeric(10,2)|Not Null|<p>Carat Of Diamond </p><p>(18 Crt,22 Crt,etc…)</p>|
|Dim\_Pcs|Numeric(10,2)|Not Null|Total Pcs Of Diamond In Item|
|Dim\_Gm|Numeric(10,2)|Not Null|Weight Of Each Diamond(Grams)|
|Dim\_Size|Numeric(10,2)|Not Null|Size Of Each Diamond|
|Dim\_Rate|Numeric(10,2)|Not Null|Rate Of Each Diamond|
|Dim\_Amt|Numeric(10,2)|Not Null|Total Amount Of All Diamonds In Item|

1. **TABLE NAME: DimQltyMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|DimQlty\_ID|nchar(10)|Primary Key|ID Of Diamond Quality|
|DimQlty|Varchar(50)|Not Null|Quality Of Diamond (AD,FD,VVS,etc…)|

1. **TABLE NAME: GoldKrtMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|GoldType\_ID|nchar(10)|Primary Key|ID Of Gold Type|
|Gold\_Crt|Varchar(50)|Not Null|<p>Carat Of Gold </p><p>(18 Crt,22 Crt,etc…)</p>|

1. **TABLE NAME: ProdMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|Prod\_ID|nchar(10)|Primary Key|Product ID|
|Prod\_Type|Varchar(50)|Not Null|Type Of Product|

1. **TABLE NAME: StoneMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|Style\_Code|Varchar(50)|Foreign Key|Code Of Style|
|StoneQlty\_ID|Varchar(50)|Foreign Key|ID Of Stone Quality|
|Stone\_Gm|Numeric(10,2)|Not Null|Weight Of Each Stone(Grams)|
|Stone\_Pcs|Numeric(10,2)|Not Null|Total Pcs Of Stones In Item|
|Stone\_Crt|Numeric(10,2)|Not Null|Carat Of Stone|
|Stone\_Rate|Numeric(10,2)|Not Null|Rate Of Each Stone|
|Stone\_Amt|Numeric(10,2)|Not Null|Total Amount Of Stones In Item|






1. **TABLE NAME: StoneQltyMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|StoneQlty\_ID|nchar(10)|Primary Key|ID Of Stone Quality|
|StoneQlty|Varchar(50)|Not Null|<p>Quality Of Stone </p><p>(Ruby,Meena,etc…)</p>|


1. ` `**TABLE NAME: UserRegMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|userID|nchar(10)|Primary key|User ID|
|userFname|Text|Not Null|First Name Of User|
|user:Lname|Text|Not Null|Last Name Of User|
|address|varchar(Max)|Not Null|Address Of User|
|city|nvarchar(50)|Not Null|City Of User|
|state|nvarchar(50)|Not Null|State Of User|
|mobNo|Text|Not Null|Mobile Number|
|emailID|Text|Not Null|EmailID Of User|
|dob|nvarchar(50)|Not Null|Birth Date Of User|
|cdate|nvarchar(50)|Not Null|Current Date|
|password|Varchar(50)|Not Null|Password Of Users|


1. **TABLE NAME: ItemMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|Style\_Code|Varchar(50)|Primary Key|Code Of Style|
|Pairs|Numeric(3,0)|Not Null|Pairs Of Product|
|Brand\_ID|nchar(10)|Foreign Key|ID Of Particular Brand|
|Quantity|Numeric(18,0)|Not Null|Available Quantity|
|Cat\_ID|nchar(10)|Foreign Key|ID Of Category|
|Prod\_Quality|Varchar(50)|Not Null|Quality Of Product|
|Certify\_ID|nchar(10)|Foreign Key|ID Of Certification|
|Prod\_ID|nchar(10)|Foreign Key|Product ID|
|GoldType\_ID|nchar(10)|Foreign Key|ID Of Gold Type|
|Gold\_Wt|Numeric(10,3)|Not Null|Weight Of Gold|
|Stone\_Wt|Numeric(10,2)|Not Null|Weight Of Stone|
|Net\_Gold|Numeric(10,3)|Not Null|Net Gold|
|Wstg\_Per|Numeric(10,3)|Not Null|Wastage In Percentage|
|Wstg|Numeric(10,3)|Not Null|Wastage|
|Tot\_Gross\_Wt|Numeric(10,3)|Not Null |Total Gross Weight|
|Gold\_Rate|Numeric(10,2)|Not Null|Rate Of Gold|
|Gold\_Amt|Numeric(10,2)|Not Null|Amount Of Gold In Item|
|Gold\_Making|Numeric(10,2)|Not Null|Gold Making Charges|
|Stone\_Making|Numeric(10,2)|Not Null|Stone Making Charges|
|Other\_Making|Numeric(10,2)|Not Null|Other Making Charges|
|Tot\_Making|Numeric(10,2)|Not Null|Total Making Charges|
|MRP|Numeric(10,2)|Not Null|MRP Of Product (Including Stone Making,Gold Making And Other Making)|



1. **TABLE NAME: DimQltySubMst**

|Field Name|Data Type|Key|Description|
| :- | :- | :- | :- |
|DimSubType\_ID|nchar(10)|Primary Key|Sub Type ID Of Diamond|
|DimQlty|Varchar(50)|Not Null|Quality Of Diamond|


1. **TABLE NAME: DimInfoMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|DimID|nchar(10)|Primary Key|Diamond ID|
|DimType|Varchar(50)|Not Null|Type Of Diamond|
|DimSubType |Varchar(50)|Not Null|Sub Type Of Diamond|
|DimCrt|Varchar(50)|Not Null|Carat Of Diamond|
|DimPrice|nchar(50)|Not Null|Price Of Diamond|
|DimImg|Varchar(50)|Not Null|Image Of Diamond|


1. **TABLE NAME: Inquiry**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|ID|nchar(10)|Primary Key|ID Of user.|
|Name|Varchar(50)|Not Null|Name Of User.|
|City|Varchar(50)|Not Null|City Of User.|
|Contact|Nchar(10)|Not Null|Contact Number|
|EmailID|Varchar(50)|Not Null|Email ID|
|Comment|Varchar(MAX)|Not Null|Comments Of user|
|Cdate|Date|Not Null|Current Date|


1. **TABLE NAME: JewelTypeMst**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|ID|nchar(10)|Primary Key|ID Of Jewellery|
|Jewellery\_Type|Varchar(50)|Not Null|Type Of Jewellery|


1. **TABLE NAME: CartList**

|**Field Name**|**Data Type**|**Key**|**Description**|
| :- | :- | :- | :- |
|ID|nchar(10)|Primary Key|ID Of Category|
|Product\_Name|Varchar(50)|Not Null|Name Of Product|
|MRP|Numeric(10,2)|Not Null|MRP of product|

